# MAVLink-совместимая зарядная станция COEX

MAVLink-совместимая зарядная станция COEX - программно-аппаратный комплекс, базирующийся на ROS и специализированном оборудовании. Для взаимодействия с зарядной станции может быть использовано любое совместимое MAVLink-устройство или MAVLink-станция управления.

## QGroundControl

На настоящий момент работа с зарядной станцией и БПЛА одновременно возможна через [специализированную версию QGroundControl](mavlink_cs_qgc.md).

Зарядная станция отображается в QGroundControl как особое MAVLink-устройство, при переключении на которое доступен новый элемент управления, позволяющий определить текущее состояние зарядной станции.

| Состояние | Расшифровка |
| --------- | ----------- |
| Unknown | Состояние зарядной станции не определено |
| Closed | Зарядная станция закрыта |
| Opening | Зарядная станция открывается |
| Open | Зарядная станция открыта |
| Closing | Зарядная станция закрывается |

Нажатием на элемент управления можно перевести станцию в одно из двух состояний:

1. Open (зарядная станция открыта).
2. Closed (зарядная станция закрыта).

Для настройки зарядной станции используются [MAVLink-параметры](mavlink_cs_params.md).

Зарядная станция поддерживает **перезагрузку** и **сброс MAVLink-параметров в значения по умолчанию**.

При подключененном GPS/RTK модуле после завершения Survey In выполняется рассылка RTCM-потока по MAVLink.

Миссия с зарядной станции строится с [использованием дополнительных точек](mavlink_cs_mission.md).

При подключении к зарядной станции в QGroundControl доступны [нестандартные значения телеметрии](mavlink_cs_values.md).
