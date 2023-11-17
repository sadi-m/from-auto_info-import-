from auto_info import *
from typing import List

def find_by_surname_NT(data: List[AutoInfoNamedTuple], auto_surname: str) -> List[AutoInfoNamedTuple]:
    """Finds all surname with given name"""
    return [item for item in data if item.surname == auto_surname]

def find_by_code_mark_auto_NT(data: List[AutoInfoNamedTuple], auto_code_mark_auto: int) -> List[AutoInfoNamedTuple]:
    """Finds all code mark auto with given name"""
    return [item for item in data if item.code_mark_auto == auto_code_mark_auto]

def find_by_engine_power_NT(data: List[AutoInfoNamedTuple], auto_engine_power: int) -> List[AutoInfoNamedTuple]:
    """Finds all engine power with given name"""
    return [item for item in data if item.engine_power == auto_engine_power]

def find_by_surname_TD(data: List[AutoInfoTypedDict], auto_surname: str) -> List[AutoInfoTypedDict]:
    """Finds all surname with given name"""
    return [item for item in data if item['surname'] == auto_surname]

def find_by_code_mark_auto_TD(data: List[AutoInfoTypedDict], auto_code_mark_auto: int) -> List[AutoInfoTypedDict]:
    """Finds all code mark auto with given name"""
    return [item for item in data if item['code_mark_auto'] == auto_code_mark_auto]

def find_by_engine_power_TD(data: List[AutoInfoTypedDict], auto_engine_power: str) -> List[AutoInfoTypedDict]:
    """Finds all engine power with given name"""
    return [item for item in data if item['engine_power'] == auto_engine_power]

def find_by_surname(data: List[AutoInfo], auto_surname: str) -> List[AutoInfo]:
    """Finds all surname with given name"""
    return [item for item in data if item.surname == auto_surname]

def find_by_code_mark_auto(data: List[AutoInfo], auto_code_mark_auto: int) -> List[AutoInfo]:
    """Finds all code mark auto with given name"""
    return [item for item in data if item.code_mark_auto == auto_code_mark_auto]

def find_by_engine_power(data: List[AutoInfo], auto_engine_power: str) -> List[AutoInfo]:
    """Finds all engine power with given name"""
    return [item for item in data if item.engine_power == auto_engine_power]

if __name__ == "__main__":
    #Auto_one = AutoInfo('maruf', 1117, 'BMW M5', 92, 81, 50, 25, 3.1)
    #Auto_two  = AutoInfo('komilov', 2015, 'KIA Rio', 92, 100, 43, 10, 3.5)
    #Auto_three  = AutoInfo('mirjonov', 2109, 'BMW', 92, 78, 39 , 20 , 4 )
    Auto_one = AutoInfoTypedDict(surname='maruf', code_mark_auto=1117, mark_auto='BMW M5', fuel=92,
                                 engine_power=81, tank_volume=50, gasoline_remaining=25, oil_volume=3.1)
    Auto_two = AutoInfoTypedDict(surname='komilov', code_mark_auto=2015, mark_auto='KIA Rio', fuel=92,
                                 engine_power=100, tank_volume=43, gasoline_remaining=10, oil_volume=3.5)
    Auto_three = AutoInfoTypedDict(surname='mirjonov', code_mark_auto=2109, mark_auto='BMW', fuel=92,
                                 engine_power=78, tank_volume=39, gasoline_remaining=20, oil_volume=4)
    data = [Auto_one, Auto_two, Auto_three]

    print(find_by_surname_TD(data, 'maruf'))
    print(find_by_surname_TD(data, 'komilov'))
    print(find_by_surname_TD(data, 'mirjonov'))

    print(find_by_code_mark_auto_TD(data, 1117))
    print(find_by_code_mark_auto_TD(data, 2015))
    print(find_by_code_mark_auto_TD(data, 2109))
    
    print(find_by_engine_power_TD(data, 81))
    print(find_by_engine_power_TD(data, 100))
    print(find_by_engine_power_TD(data, 78))
