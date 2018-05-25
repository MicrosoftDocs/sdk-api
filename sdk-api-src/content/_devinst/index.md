---
UID: TP:devinst
ms.assetid: a4a2af86-b619-3628-9589-89ded9b021bd
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Device and Driver Installation Reference



Overview of the Device and Driver Installation Reference technology.

To develop Device and Driver Installation Reference, you need these headers:

 * [cfg.h](..\cfg\index.md)
 * [cfgmgr32.h](..\cfgmgr32\index.md)
 * [difxapi.h](..\difxapi\index.md)
 * [newdev.h](..\newdev\index.md)

For the programming guide, see [Device and Driver Installation Reference](/windows/desktop/devinst).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CM_Add_Empty_Log_Conf function](..\cfgmgr32\nf-cfgmgr32-cm_add_empty_log_conf.md) | The CM_Add_Empty_Log_Conf function creates an empty logical configuration, for a specified configuration type and a specified device instance, on the local machine. |
| [CM_Add_Empty_Log_Conf_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_add_empty_log_conf_ex.md) | The CM_Add_Empty_Log_Conf_Ex function creates an empty logical configuration, for a specified configuration type and a specified device instance, on either the local or a remote machine. |
| [CM_Add_IDW function](..\cfgmgr32\nf-cfgmgr32-cm_add_idw.md) | The CM_Add_ID function appends a specified device ID (if not already present) to a device instance's&#160;hardware ID list or compatible ID list. |
| [CM_Add_ID_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_add_id_exw.md) | The CM_Add_ID_Ex function appends a device ID (if not already present) to a device instance's hardware ID list or compatible ID list, on either the local or a remote machine. |
| [CM_Add_Res_Des function](..\cfgmgr32\nf-cfgmgr32-cm_add_res_des.md) | The CM_Add_Res_Des function adds a resource descriptor to a logical configuration. |
| [CM_Add_Res_Des_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_add_res_des_ex.md) | The CM_Add_Res_Des_Ex function adds a resource descriptor to a logical configuration. The logical configuration can be on either the local or a remote machine. |
| [CM_Connect_MachineW function](..\cfgmgr32\nf-cfgmgr32-cm_connect_machinew.md) | The CM_Connect_Machine function creates a connection to a remote machine. |
| [CM_Delete_Class_Key function](..\cfgmgr32\nf-cfgmgr32-cm_delete_class_key.md) | The CM_Delete_Class_Key function removes the specified installed device class from the system. |
| [CM_Delete_DevNode_Key function](..\cfgmgr32\nf-cfgmgr32-cm_delete_devnode_key.md) | The CM_Delete_DevNode_Key function deletes the specified user-accessible registry keys that are associated with a device. |
| [CM_Delete_Device_Interface_KeyW function](..\cfgmgr32\nf-cfgmgr32-cm_delete_device_interface_keyw.md) | The CM_Delete_Device_Interface_Key function deletes the registry subkey that is used by applications and drivers to store interface-specific information. |
| [CM_Delete_Device_Interface_Key_ExA function](..\cfgmgr32\nf-cfgmgr32-cm_delete_device_interface_key_exa.md) | The CM_Delete_Device_Interface_Key_ExA function deletes the registry subkey that is used by applications and drivers to store interface-specific information. |
| [CM_Delete_Device_Interface_Key_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_delete_device_interface_key_exw.md) | The CM_Delete_Device_Interface_Key_ExW function deletes the registry subkey that is used by applications and drivers to store interface-specific information. |
| [CM_Disable_DevNode function](..\cfgmgr32\nf-cfgmgr32-cm_disable_devnode.md) | The CM_Disable_DevNode function disables a device. |
| [CM_Disconnect_Machine function](..\cfgmgr32\nf-cfgmgr32-cm_disconnect_machine.md) | The CM_Disconnect_Machine function removes a connection to a remote machine. |
| [CM_Enable_DevNode function](..\cfgmgr32\nf-cfgmgr32-cm_enable_devnode.md) | The CM_Enable_DevNode function enables a device. |
| [CM_Enumerate_Classes function](..\cfgmgr32\nf-cfgmgr32-cm_enumerate_classes.md) | The CM_Enumerate_Classes function, when called repeatedly, enumerates the local machine's installed device classes by supplying each class's GUID. |
| [CM_Enumerate_Classes_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_enumerate_classes_ex.md) | The CM_Enumerate_Classes_Ex function, when called repeatedly, enumerates a local or a remote machine's installed device classes, by supplying each class's GUID. |
| [CM_Enumerate_EnumeratorsW function](..\cfgmgr32\nf-cfgmgr32-cm_enumerate_enumeratorsw.md) | The CM_Enumerate_Enumerators function enumerates the local machine's device enumerators by supplying each enumerator's name. |
| [CM_Enumerate_Enumerators_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_enumerate_enumerators_exw.md) | The CM_Enumerate_Enumerators_Ex function enumerates a local or a remote machine's device enumerators, by supplying each enumerator's name. |
| [CM_Free_Log_Conf function](..\cfgmgr32\nf-cfgmgr32-cm_free_log_conf.md) | The CM_Free_Log_Conf function removes a logical configuration and all associated resource descriptors from the local machine. |
| [CM_Free_Log_Conf_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_free_log_conf_ex.md) | The CM_Free_Log_Conf_Ex function removes a logical configuration and all associated resource descriptors from either a local or a remote machine. |
| [CM_Free_Log_Conf_Handle function](..\cfgmgr32\nf-cfgmgr32-cm_free_log_conf_handle.md) | The CM_Free_Log_Conf_Handle function invalidates a logical configuration handle and frees its associated memory allocation. |
| [CM_Free_Res_Des function](..\cfgmgr32\nf-cfgmgr32-cm_free_res_des.md) | The CM_Free_Res_Des function removes a resource descriptor from a logical configuration on the local machine. |
| [CM_Free_Res_Des_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_free_res_des_ex.md) | The CM_Free_Res_Des_Ex function removes a resource descriptor from a logical configuration on either a local or a remote machine. |
| [CM_Free_Res_Des_Handle function](..\cfgmgr32\nf-cfgmgr32-cm_free_res_des_handle.md) | The CM_Free_Res_Des_Handle function invalidates a resource description handle and frees its associated memory allocation. |
| [CM_Free_Resource_Conflict_Handle function](..\cfgmgr32\nf-cfgmgr32-cm_free_resource_conflict_handle.md) | The CM_Free_Resource_Conflict_Handle function invalidates a handle to a resource conflict list, and frees the handle's associated memory allocation. |
| [CM_Get_Child function](..\cfgmgr32\nf-cfgmgr32-cm_get_child.md) | The CM_Get_Child function is used to retrieve a device instance handle to the first child node of a specified device node (devnode) in the local machine's device tree. |
| [CM_Get_Child_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_child_ex.md) | The CM_Get_Child_Ex function is used to retrieve a device instance handle to the first child node of a specified device node (devnode) in a local or a remote machine's device tree. |
| [CM_Get_Class_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_get_class_propertyw.md) | The CM_Get_Class_Property function retrieves a device property that is set for a device interface class or device setup class. |
| [CM_Get_Class_Property_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_class_property_exw.md) | The CM_Get_Class_Property_ExW function retrieves a device property that is set for a device interface class or device setup class. |
| [CM_Get_Class_Property_Keys function](..\cfgmgr32\nf-cfgmgr32-cm_get_class_property_keys.md) | The CM_Get_Class_Property_Keys function retrieves an array of the device property keys that represent the device properties that are set for a device interface class or device setup class. |
| [CM_Get_Class_Property_Keys_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_class_property_keys_ex.md) | The CM_Get_Class_Property_Keys_Ex function retrieves an array of the device property keys that represent the device properties that are set for a device interface class or device setup class. |
| [CM_Get_Class_Registry_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_get_class_registry_propertyw.md) | The CM_Get_Class_Registry_Property function retrieves a device setup class property. |
| [CM_Get_Depth function](..\cfgmgr32\nf-cfgmgr32-cm_get_depth.md) | The CM_Get_Depth function is used to obtain the depth of a specified device node (devnode) within the local machine's device tree. |
| [CM_Get_Depth_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_depth_ex.md) | The CM_Get_Depth_Ex function is used to obtain the depth of a specified device node (devnode) within a local or a remote machine's device tree. |
| [CM_Get_DevNode_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_get_devnode_propertyw.md) | The CM_Get_DevNode_Property function retrieves a device instance property. |
| [CM_Get_DevNode_Property_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_devnode_property_exw.md) | The CM_Get_DevNode_Property_ExW function retrieves a device instance property. |
| [CM_Get_DevNode_Property_Keys function](..\cfgmgr32\nf-cfgmgr32-cm_get_devnode_property_keys.md) | The CM_Get_DevNode_Property_Keys function retrieves an array of the device property keys that represent the device properties that are set for a device instance. |
| [CM_Get_DevNode_Property_Keys_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_devnode_property_keys_ex.md) | The CM_Get_DevNode_Property_Keys_Ex function retrieves an array of the device property keys that represent the device properties that are set for a device instance. |
| [CM_Get_DevNode_Registry_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_get_devnode_registry_propertyw.md) | The CM_Get_DevNode_Registry_Property function retrieves a specified device property from the registry. |
| [CM_Get_DevNode_Status function](..\cfgmgr32\nf-cfgmgr32-cm_get_devnode_status.md) | The CM_Get_DevNode_Status function obtains the status of a device instance from its device node (devnode) in the local machine's device tree. |
| [CM_Get_DevNode_Status_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_devnode_status_ex.md) | The CM_Get_DevNode_Status_Ex function obtains the status of a device instance from its device node (devnode) on a local or a remote machine's device tree. |
| [CM_Get_Device_IDW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_idw.md) | The CM_Get_Device_ID function retrieves the device instance ID for a specified device instance on the local machine. |
| [CM_Get_Device_ID_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_exw.md) | The CM_Get_Device_ID_Ex function retrieves the device instance ID for a specified device instance on a local or a remote machine. |
| [CM_Get_Device_ID_ListA function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_lista.md) | The CM_Get_Device_ID_List function retrieves a list of device instance IDs for the local computer's device instances. |
| [CM_Get_Device_ID_ListW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_listw.md) | The CM_Get_Device_ID_List function retrieves a list of device instance IDs for the local computer's device instances. |
| [CM_Get_Device_ID_List_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_list_exw.md) | The CM_Get_Device_ID_List_Ex function retrieves a list of device instance IDs for the device instances on a local or a remote machine. |
| [CM_Get_Device_ID_List_SizeA function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_list_sizea.md) | The CM_Get_Device_ID_List_Size function retrieves the buffer size required to hold a list of device instance IDs for the local machine's device instances. |
| [CM_Get_Device_ID_List_SizeW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_list_sizew.md) | The CM_Get_Device_ID_List_Size function retrieves the buffer size required to hold a list of device instance IDs for the local machine's device instances. |
| [CM_Get_Device_ID_List_Size_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_list_size_exw.md) | The CM_Get_Device_ID_List_Size_Ex function retrieves the buffer size required to hold a list of device instance IDs for a local or a remote machine's device instances. |
| [CM_Get_Device_ID_Size function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_size.md) | The CM_Get_Device_ID_Size function retrieves the buffer size required to hold a device instance ID for a device instance on the local machine. |
| [CM_Get_Device_ID_Size_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_id_size_ex.md) | The CM_Get_Device_ID_Size_Ex function retrieves the buffer size required to hold a device instance ID for a device instance on a local or a remote machine. |
| [CM_Get_Device_Interface_AliasW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_aliasw.md) | The CM_Get_Device_Interface_Alias function returns the alias of the specified device interface instance, if the alias exists. |
| [CM_Get_Device_Interface_ListA function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_lista.md) | The CM_Get_Device_Interface_List function retrieves a list of device interface instances that belong to a specified device interface class. |
| [CM_Get_Device_Interface_ListW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_listw.md) | The CM_Get_Device_Interface_List function retrieves a list of device interface instances that belong to a specified device interface class. |
| [CM_Get_Device_Interface_List_SizeA function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_list_sizea.md) | The CM_Get_Device_Interface_List_Size function retrieves the buffer size that must be passed to the CM_Get_Device_Interface_List function. |
| [CM_Get_Device_Interface_List_SizeW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_list_sizew.md) | The CM_Get_Device_Interface_List_Size function retrieves the buffer size that must be passed to the CM_Get_Device_Interface_List function. |
| [CM_Get_Device_Interface_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_propertyw.md) | The CM_Get_Device_Interface_Property function retrieves a device property that is set for a device interface. |
| [CM_Get_Device_Interface_Property_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_property_exw.md) | The CM_Get_Device_Interface_Property_ExW function retrieves a device property that is set for a device interface. |
| [CM_Get_Device_Interface_Property_KeysW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_property_keysw.md) | The CM_Get_Device_Interface_Property_Keys function retrieves an array of device property keys that represent the device properties that are set for a device interface. |
| [CM_Get_Device_Interface_Property_Keys_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_device_interface_property_keys_exw.md) | The CM_Get_Device_Interface_Property_Keys_ExW function retrieves an array of device property keys that represent the device properties that are set for a device interface. |
| [CM_Get_First_Log_Conf function](..\cfgmgr32\nf-cfgmgr32-cm_get_first_log_conf.md) | The CM_Get_First_Log_Conf function obtains the first logical configuration, of a specified configuration type, associated with a specified device instance on the local machine. |
| [CM_Get_First_Log_Conf_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_first_log_conf_ex.md) | The CM_Get_First_Log_Conf_Ex function obtains the first logical configuration associated with a specified device instance on a local or a remote machine. |
| [CM_Get_HW_Prof_FlagsA function](..\cfgmgr32\nf-cfgmgr32-cm_get_hw_prof_flagsa.md) | The CM_Get_HW_Prof_Flags function retrieves the hardware profile-specific configuration flags for a device instance on a local machine. |
| [CM_Get_HW_Prof_FlagsW function](..\cfgmgr32\nf-cfgmgr32-cm_get_hw_prof_flagsw.md) | The CM_Get_HW_Prof_Flags function retrieves the hardware profile-specific configuration flags for a device instance on a local machine. |
| [CM_Get_HW_Prof_Flags_ExA function](..\cfgmgr32\nf-cfgmgr32-cm_get_hw_prof_flags_exa.md) | The CM_Get_HW_Prof_Flags_Ex function retrieves the hardware profile-specific configuration flags for a device instance on a remote machine or a local machine. |
| [CM_Get_HW_Prof_Flags_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_get_hw_prof_flags_exw.md) | The CM_Get_HW_Prof_Flags_Ex function retrieves the hardware profile-specific configuration flags for a device instance on a remote machine or a local machine. |
| [CM_Get_Log_Conf_Priority function](..\cfgmgr32\nf-cfgmgr32-cm_get_log_conf_priority.md) | The CM_Get_Log_Conf_Priority function obtains the configuration priority of a specified logical configuration on the local machine. |
| [CM_Get_Log_Conf_Priority_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_log_conf_priority_ex.md) | The CM_Get_Log_Conf_Priority_Ex function obtains the configuration priority of a specified logical configuration on a local or a remote machine. |
| [CM_Get_Next_Log_Conf function](..\cfgmgr32\nf-cfgmgr32-cm_get_next_log_conf.md) | The CM_Get_Next_Log_Conf function obtains the next logical configuration associated with a specific device instance on the local machine. |
| [CM_Get_Next_Log_Conf_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_next_log_conf_ex.md) | The CM_Get_Next_Log_Conf_Ex function obtains the next logical configuration associated with a specific device instance on a local or a remote machine. |
| [CM_Get_Next_Res_Des function](..\cfgmgr32\nf-cfgmgr32-cm_get_next_res_des.md) | The CM_Get_Next_Res_Des function obtains a handle to the next resource descriptor, of a specified resource type, for a logical configuration on the local machine. |
| [CM_Get_Next_Res_Des_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_next_res_des_ex.md) | The CM_Get_Next_Res_Des_Ex function obtains a handle to the next resource descriptor, of a specified resource type, for a logical configuration on a local or a remote machine. |
| [CM_Get_Parent function](..\cfgmgr32\nf-cfgmgr32-cm_get_parent.md) | The CM_Get_Parent function obtains a device instance handle to the parent node of a specified device node (devnode) in the local machine's device tree. |
| [CM_Get_Parent_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_parent_ex.md) | The CM_Get_Parent_Ex function obtains a device instance handle to the parent node of a specified device node (devnode) in a local or a remote machine's device tree. |
| [CM_Get_Res_Des_Data function](..\cfgmgr32\nf-cfgmgr32-cm_get_res_des_data.md) | The CM_Get_Res_Des_Data function retrieves the information stored in a resource descriptor on the local machine. |
| [CM_Get_Res_Des_Data_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_res_des_data_ex.md) | The CM_Get_Res_Des_Data_Ex function retrieves the information stored in a resource descriptor on a local or a remote machine. |
| [CM_Get_Res_Des_Data_Size function](..\cfgmgr32\nf-cfgmgr32-cm_get_res_des_data_size.md) | The CM_Get_Res_Des_Data_Size function obtains the buffer size required to hold the information contained in a specified resource descriptor on the local machine. |
| [CM_Get_Res_Des_Data_Size_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_res_des_data_size_ex.md) | The CM_Get_Res_Des_Data_Size_Ex function obtains the buffer size required to hold the information contained in a specified resource descriptor on a local or a remote machine. |
| [CM_Get_Resource_Conflict_Count function](..\cfgmgr32\nf-cfgmgr32-cm_get_resource_conflict_count.md) | The CM_Get_Resource_Conflict_Count function obtains the number of conflicts contained in a specified resource conflict list. |
| [CM_Get_Resource_Conflict_DetailsW function](..\cfgmgr32\nf-cfgmgr32-cm_get_resource_conflict_detailsw.md) | The CM_Get_Resource_Conflict_Details function obtains the details about one of the resource conflicts in a conflict list. |
| [CM_Get_Sibling function](..\cfgmgr32\nf-cfgmgr32-cm_get_sibling.md) | The CM_Get_Sibling function obtains a device instance handle to the next sibling node of a specified device node (devnode) in the local machine's device tree. |
| [CM_Get_Sibling_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_sibling_ex.md) | The CM_Get_Sibling_Ex function obtains a device instance handle to the next sibling node of a specified device node, in a local or a remote machine's device tree. |
| [CM_Get_Version function](..\cfgmgr32\nf-cfgmgr32-cm_get_version.md) | The CM_Get_Version function returns version 4.0 of the Plug and Play (PnP) Configuration Manager DLL (Cfgmgr32.dll) for a local machine. |
| [CM_Get_Version_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_get_version_ex.md) | The CM_Get_Version_Ex function returns version 4.0 of the Plug and Play (PnP) Configuration Manager DLL (Cfgmgr32.dll) for a local or a remote machine. |
| [CM_Is_Dock_Station_Present function](..\cfgmgr32\nf-cfgmgr32-cm_is_dock_station_present.md) | The CM_Is_Dock_Station_Present function identifies whether a docking station is present in a local machine. |
| [CM_Is_Dock_Station_Present_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_is_dock_station_present_ex.md) | The CM_Is_Dock_Station_Present_Ex function identifies whether a docking station is present in a local or a remote machine. |
| [CM_Is_Version_Available function](..\cfgmgr32\nf-cfgmgr32-cm_is_version_available.md) | The CM_Is_Version_Available function indicates whether a specified version of the Plug and Play (PnP) Configuration Manager DLL (Cfgmgr32.dll) is supported by a local machine. |
| [CM_Is_Version_Available_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_is_version_available_ex.md) | The CM_Is_Version_Available_Ex function indicates whether a specified version of the Plug and Play (PNP) Configuration Manager DLL (Cfgmgr32.dll) is supported by a local or a remote machine. |
| [CM_Locate_DevNodeA function](..\cfgmgr32\nf-cfgmgr32-cm_locate_devnodea.md) | The CM_Locate_DevNode function obtains a device instance handle to the device node that is associated with a specified device instance ID on the local machine. |
| [CM_Locate_DevNodeW function](..\cfgmgr32\nf-cfgmgr32-cm_locate_devnodew.md) | The CM_Locate_DevNode function obtains a device instance handle to the device node that is associated with a specified device instance ID on the local machine. |
| [CM_Locate_DevNode_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_locate_devnode_exw.md) | The CM_Locate_DevNode_Ex function obtains a device instance handle to the device node that is associated with a specified device instance ID, on a local machine or a remote machine. |
| [CM_MapCrToWin32Err function](..\cfgmgr32\nf-cfgmgr32-cm_mapcrtowin32err.md) | Converts a specified CONFIGRET code to its equivalent system error code. |
| [CM_Modify_Res_Des function](..\cfgmgr32\nf-cfgmgr32-cm_modify_res_des.md) | The CM_Modify_Res_Des function modifies a specified resource descriptor on the local machine. |
| [CM_Modify_Res_Des_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_modify_res_des_ex.md) | The CM_Modify_Res_Des_Ex function modifies a specified resource descriptor on a local or a remote machine. |
| [CM_Open_Class_KeyW function](..\cfgmgr32\nf-cfgmgr32-cm_open_class_keyw.md) | The CM_Open_Class_Key function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class. |
| [CM_Open_DevNode_Key function](..\cfgmgr32\nf-cfgmgr32-cm_open_devnode_key.md) | The CM_Open_DevNode_Key function opens a registry key for device-specific configuration information. |
| [CM_Open_Device_Interface_KeyA function](..\cfgmgr32\nf-cfgmgr32-cm_open_device_interface_keya.md) | The CM_Open_Device_Interface_Key function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface. |
| [CM_Open_Device_Interface_KeyW function](..\cfgmgr32\nf-cfgmgr32-cm_open_device_interface_keyw.md) | The CM_Open_Device_Interface_Key function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface. |
| [CM_Open_Device_Interface_Key_ExA function](..\cfgmgr32\nf-cfgmgr32-cm_open_device_interface_key_exa.md) | The CM_Open_Device_Interface_Key_ExA function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface. |
| [CM_Open_Device_Interface_Key_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_open_device_interface_key_exw.md) | The CM_Open_Device_Interface_Key_ExW function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface. |
| [CM_Query_And_Remove_SubTreeW function](..\cfgmgr32\nf-cfgmgr32-cm_query_and_remove_subtreew.md) | The CM_Query_And_Remove_SubTree function checks whether a device instance and its children can be removed and, if so, it removes them. |
| [CM_Query_And_Remove_SubTree_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_query_and_remove_subtree_exw.md) | The CM_Query_And_Remove_SubTree_Ex function checks whether a device instance and its children can be removed and, if so, it removes them. |
| [CM_Query_Resource_Conflict_List function](..\cfgmgr32\nf-cfgmgr32-cm_query_resource_conflict_list.md) | The CM_Query_Resource_Conflict_List function identifies device instances having resource requirements that conflict with a specified device instance's resource description. |
| [CM_Reenumerate_DevNode function](..\cfgmgr32\nf-cfgmgr32-cm_reenumerate_devnode.md) | The CM_Reenumerate_DevNode function enumerates the devices identified by a specified device node and all of its children. |
| [CM_Reenumerate_DevNode_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_reenumerate_devnode_ex.md) | The CM_Reenumerate_DevNode_Ex function enumerates the devices identified by a specified device node and all of its children. |
| [CM_Register_Notification function](..\cfgmgr32\nf-cfgmgr32-cm_register_notification.md) | Use RegisterDeviceNotification instead of CM_Register_Notification if your code targets Windows 7 or earlier versions of Windows. Kernel mode callers should use IoRegisterPlugPlayNotification instead. |
| [CM_Request_Device_EjectW function](..\cfgmgr32\nf-cfgmgr32-cm_request_device_ejectw.md) | The CM_Request_Device_Eject function prepares a local device instance for safe removal, if the device is removable. If the device can be physically ejected, it will be. |
| [CM_Request_Device_Eject_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_request_device_eject_exw.md) | The CM_Request_Device_Eject_Ex function prepares a local or a remote device instance for safe removal, if the device is removable. If the device can be physically ejected, it will be. |
| [CM_Request_Eject_PC function](..\cfgmgr32\nf-cfgmgr32-cm_request_eject_pc.md) | The CM_Request_Eject_PC function requests that a portable PC, which is inserted in a local docking station, be ejected. |
| [CM_Request_Eject_PC_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_request_eject_pc_ex.md) | The CM_Request_Eject_PC_Ex function requests that a portable PC, which is inserted in a local or a remote docking station, be ejected. |
| [CM_Set_Class_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_set_class_propertyw.md) | The CM_Set_Class_Property function sets a class property for a device setup class or a device interface class. |
| [CM_Set_Class_Property_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_set_class_property_exw.md) | The CM_Set_Class_Property_ExW function sets a class property for a device setup class or a device interface class. |
| [CM_Set_Class_Registry_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_set_class_registry_propertyw.md) | The CM_Set_Class_Registry_Property function sets or deletes a property of a device setup class. |
| [CM_Set_DevNode_Problem function](..\cfgmgr32\nf-cfgmgr32-cm_set_devnode_problem.md) | The CM_Set_DevNode_Problem function sets a problem code for a device that is installed in a local machine. |
| [CM_Set_DevNode_Problem_Ex function](..\cfgmgr32\nf-cfgmgr32-cm_set_devnode_problem_ex.md) | The CM_Set_DevNode_Problem_Ex function sets a problem code for a device that is installed in a local or a remote machine. |
| [CM_Set_DevNode_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_set_devnode_propertyw.md) | The CM_Set_DevNode_Property function sets a device instance property. |
| [CM_Set_DevNode_Property_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_set_devnode_property_exw.md) | The CM_Set_DevNode_Property_ExW function sets a device instance property. |
| [CM_Set_DevNode_Registry_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_set_devnode_registry_propertyw.md) | The CM_Set_DevNode_Registry_Property function sets a specified device property in the registry. |
| [CM_Set_Device_Interface_PropertyW function](..\cfgmgr32\nf-cfgmgr32-cm_set_device_interface_propertyw.md) | The CM_Set_Device_Interface_Property function sets a device property of a device interface. |
| [CM_Set_Device_Interface_Property_ExW function](..\cfgmgr32\nf-cfgmgr32-cm_set_device_interface_property_exw.md) | The CM_Set_Device_Interface_Property_ExW function sets a device property of a device interface. |
| [CM_Setup_DevNode function](..\cfgmgr32\nf-cfgmgr32-cm_setup_devnode.md) | The CM_Setup_DevNode function restarts a device instance that is not running because there is a problem with the device configuration. |
| [CM_Uninstall_DevNode function](..\cfgmgr32\nf-cfgmgr32-cm_uninstall_devnode.md) | The CM_Uninstall_DevNode function removes all persistent state associated with a device instance. |
| [CM_Unregister_Notification function](..\cfgmgr32\nf-cfgmgr32-cm_unregister_notification.md) | Use UnregisterDeviceNotification instead of CM_Unregister_Notification if your code targets Windows 7 or earlier versions of Windows. |
| [DiInstallDevice function](..\newdev\nf-newdev-diinstalldevice.md) | The DiInstallDevice function installs a specified driver that is preinstalled in the driver store on a specified device that is present in the system. |
| [DiRollbackDriver function](..\newdev\nf-newdev-dirollbackdriver.md) | The DiRollbackDriver function rolls back the driver that is installed on a specified device. |
| [DiShowUpdateDevice function](..\newdev\nf-newdev-dishowupdatedevice.md) | The DiShowUpdateDevice function displays the Hardware Update wizard for a specified device. |
| [DiUninstallDevice function](..\newdev\nf-newdev-diuninstalldevice.md) | The DiUninstallDevice function uninstalls a device and removes its device node (devnode) from the system. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [BusNumber_Des_s structure](..\cfgmgr32\ns-cfgmgr32-busnumber_des_s.md) | The BUSNUMBER_DES structure is used for specifying either a resource list or a resource requirements list that describes bus number usage for a device instance. |
| [BusNumber_Range_s structure](..\cfgmgr32\ns-cfgmgr32-busnumber_range_s.md) | The BUSNUMBER_RANGE structure specifies a resource requirements list that describes bus number usage for a device instance. For more information about resource requirements lists, see Hardware Resources. |
| [BusNumber_Resource_s structure](..\cfgmgr32\ns-cfgmgr32-busnumber_resource_s.md) | The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources. |
| [CS_Des_s structure](..\cfgmgr32\ns-cfgmgr32-cs_des_s.md) | The CS_DES structure is used for specifying a resource list that describes device class-specific resource usage for a device instance. For more information about resource lists, see Hardware Resources. |
| [CS_Resource_s structure](..\cfgmgr32\ns-cfgmgr32-cs_resource_s.md) | The CS_RESOURCE structure is used for specifying a resource list that describes device class-specific resource usage for a device instance. For more information about resource lists, see Hardware Resources. |
| [DMA_Des_s structure](..\cfgmgr32\ns-cfgmgr32-dma_des_s.md) | The DMA_DES structure is used for specifying either a resource list or a resource requirements list that describes direct memory access (DMA) channel usage for a device instance. |
| [DMA_Range_s structure](..\cfgmgr32\ns-cfgmgr32-dma_range_s.md) | The DMA_RANGE structure specifies a resource requirements list that describes DMA channel usage for a device instance. For more information about resource requirements lists, see Hardware Resources. |
| [DMA_Resource_s structure](..\cfgmgr32\ns-cfgmgr32-dma_resource_s.md) | The DMA_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes DMA channel usage for a device instance. |
| [INSTALLERINFO_A structure](..\difxapi\ns-difxapi-installerinfo_a.md) | The INSTALLERINFO structure contains information about an application that DIFxAPI associates with a driver package. |
| [INSTALLERINFO_W structure](..\difxapi\ns-difxapi-installerinfo_w.md) | The INSTALLERINFO structure contains information about an application that DIFxAPI associates with a driver package. |
| [IO_Des_s structure](..\cfgmgr32\ns-cfgmgr32-io_des_s.md) | The IO_DES structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources. |
| [IO_Range_s structure](..\cfgmgr32\ns-cfgmgr32-io_range_s.md) | The IO_RANGE structure specifies a resource requirements list that describes I/O port usage for a device instance. For more information about resource requirements lists, see Hardware Resources. |
| [IO_Resource_s structure](..\cfgmgr32\ns-cfgmgr32-io_resource_s.md) | The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance. |
| [IRQ_Des_32_s structure](..\cfgmgr32\ns-cfgmgr32-irq_des_32_s.md) | The IRQ_DES structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources. |
| [IRQ_Des_64_s structure](..\cfgmgr32\ns-cfgmgr32-irq_des_64_s.md) | The IRQ_DES structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources. |
| [IRQ_Range_s structure](..\cfgmgr32\ns-cfgmgr32-irq_range_s.md) | The IRQ_RANGE structure specifies a resource requirements list that describes IRQ line usage for a device instance. For more information about resource requirements lists, see Hardware Resources. |
| [IRQ_Resource_32_s structure](..\cfgmgr32\ns-cfgmgr32-irq_resource_32_s.md) | The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. |
| [IRQ_Resource_64_s structure](..\cfgmgr32\ns-cfgmgr32-irq_resource_64_s.md) | The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. |
| [Mem_Des_s structure](..\cfgmgr32\ns-cfgmgr32-mem_des_s.md) | The MEM_DES structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources. |
| [Mem_Range_s structure](..\cfgmgr32\ns-cfgmgr32-mem_range_s.md) | The MEM_RANGE structure specifies a resource requirements list that describes memory usage for a device instance. For more information about resource requirements lists, see Hardware Resources. |
| [Mem_Resource_s structure](..\cfgmgr32\ns-cfgmgr32-mem_resource_s.md) | The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance. For more information about resource lists and resource requirements lists, see Hardware Resources. |
| [MfCard_Des_s structure](..\cfgmgr32\ns-cfgmgr32-mfcard_des_s.md) | The MFCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by one of the hardware functions provided by an instance of a multifunction device. |
| [MfCard_Resource_s structure](..\cfgmgr32\ns-cfgmgr32-mfcard_resource_s.md) | The MFCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by one of the hardware functions provided by an instance of a multifunction device. |
| [PcCard_Des_s structure](..\cfgmgr32\ns-cfgmgr32-pccard_des_s.md) | The PCCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance. For more information about resource lists and resource requirements lists, see Hardware Resources. |
| [PcCard_Resource_s structure](..\cfgmgr32\ns-cfgmgr32-pccard_resource_s.md) | The PCCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance. |
| [_CM_NOTIFY_EVENT_DATA structure](..\cfgmgr32\ns-cfgmgr32-_cm_notify_event_data.md) | This is a device notification event data structure. |
| [_CM_NOTIFY_FILTER structure](..\cfgmgr32\ns-cfgmgr32-_cm_notify_filter.md) | Device notification filter structure. |
| [_CONFLICT_DETAILS_A structure](..\cfgmgr32\ns-cfgmgr32-_conflict_details_a.md) | The CONFLICT_DETAILS structure is used as a parameter to the CM_Get_Resource_Conflict_Details function. |
| [_CONFLICT_DETAILS_W structure](..\cfgmgr32\ns-cfgmgr32-_conflict_details_w.md) | The CONFLICT_DETAILS structure is used as a parameter to the CM_Get_Resource_Conflict_Details function. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_CM_NOTIFY_ACTION enumeration](..\cfgmgr32\ne-cfgmgr32-_cm_notify_action.md) | This enumeration identifies Plug and Play device event types. |
| [_PNP_VETO_TYPE enumeration](..\cfg\ne-cfg-_pnp_veto_type.md) | If the PnP manager rejects a request to perform an operation, the PNP_VETO_TYPE enumeration is used to identify the reason for the rejection. |
