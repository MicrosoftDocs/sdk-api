---
UID: NF:cfgmgr32.CM_Get_Device_Interface_ListA
title: CM_Get_Device_Interface_ListA function (cfgmgr32.h)
description: The CM_Get_Device_Interface_List function retrieves a list of device interface instances that belong to a specified device interface class. (ANSI)
helpviewer_keywords: ["CM_Get_Device_Interface_ListA", "cfgmgr32/CM_Get_Device_Interface_ListA", "cfgmgrfn_8729dc17-f9a0-4ebe-ad56-35c63f9299f0.xml"]
old-location: devinst\cm_get_device_interface_list.htm
tech.root: devinst
ms.assetid: 3f2dfc0f-1bde-40a8-b48c-25b75759e0d8
ms.date: 12/05/2018
ms.keywords: CM_Get_Device_Interface_List, CM_Get_Device_Interface_List function [Device and Driver Installation], CM_Get_Device_Interface_ListA, CM_Get_Device_Interface_ListW, cfgmgr32/CM_Get_Device_Interface_List, cfgmgr32/CM_Get_Device_Interface_ListA, cfgmgr32/CM_Get_Device_Interface_ListW, cfgmgrfn_8729dc17-f9a0-4ebe-ad56-35c63f9299f0.xml, devinst.cm_get_device_interface_list
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_Interface_ListW (Unicode) and CM_Get_Device_Interface_ListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Device_Interface_ListA
 - cfgmgr32/CM_Get_Device_Interface_ListA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-config-l1-1-2.dll
 - CfgMgr32.dll
 - API-MS-Win-Devices-Config-L1-1-0.dll
 - API-MS-Win-Devices-Config-L1-1-1.dll
api_name:
 - CM_Get_Device_Interface_List
 - CM_Get_Device_Interface_ListA
 - CM_Get_Device_Interface_ListW
---

# CM_Get_Device_Interface_ListA function


## -description

The <b>CM_Get_Device_Interface_List</b> function retrieves a list of device interface instances that belong to a specified <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a>.

## -parameters

### -param InterfaceClassGuid [in]

Supplies a GUID that identifies a device interface class.

### -param pDeviceID [in, optional]

Caller-supplied pointer to a NULL-terminated string that represents a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>. If specified, the function retrieves device interfaces that are supported by the device for the specified class. If this value is <b>NULL</b>, or if it points to a zero-length string, the function retrieves all interfaces that belong to the specified class.

### -param Buffer [out]

Caller-supplied pointer to a buffer that receives multiple, NULL-terminated Unicode strings, each representing the symbolic link name of an interface instance.

### -param BufferLen [in]

Caller-supplied value that specifies the length, in characters, of the buffer pointed to by <i>Buffer</i>. Call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea">CM_Get_Device_Interface_List_Size</a> to determine the required buffer size.

### -param ulFlags [in]

Contains one of the following caller-supplied flags:





#### CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES

The function provides a list containing device interfaces associated with all devices that match the specified GUID and device instance ID, if any.



#### CM_GET_DEVICE_INTERFACE_LIST_PRESENT

The function provides a list containing device interfaces associated with devices that are currently active, and which match the specified GUID and device instance ID, if any.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the error codes with the CR_ prefix as defined in <i>Cfgmgr32.h</i>.

The following table includes some of the more common error codes that this function might return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_BUFFER_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>Buffer</i> buffer is too small to hold the requested list of device interfaces.

</td>
</tr>
</table>

## -remarks

Between calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea">CM_Get_Device_Interface_List_Size</a> to get the size of the list and calling <b>CM_Get_Device_Interface_List</b> to get the list, a new device interface can be added to the system causing the size returned to no longer be valid.  Callers should be robust to that condition and retry getting the size and the list if <b>CM_Get_Device_Interface_List</b> returns <b>CR_BUFFER_SMALL</b>.


#### Examples

This snippet illustrates retrying getting the size and the list as described in the Remarks section.


```cpp
    CONFIGRET cr = CR_SUCCESS;
    PWSTR DeviceInterfaceList = NULL;
    ULONG DeviceInterfaceListLength = 0;

    do {
        cr = CM_Get_Device_Interface_List_Size(&DeviceInterfaceListLength,
                                               (LPGUID)&GUID_DEVINTERFACE_VOLUME,
                                               NULL,
                                               CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES);

        if (cr != CR_SUCCESS)
        {
            break;
        }

        if (DeviceInterfaceList != NULL) {
            HeapFree(GetProcessHeap(),
                     0,
                     DeviceInterfaceList);
        }

        DeviceInterfaceList = (PWSTR)HeapAlloc(GetProcessHeap(),
                                               HEAP_ZERO_MEMORY,
                                               DeviceInterfaceListLength * sizeof(WCHAR));

        if (DeviceInterfaceList == NULL)
        {
            cr = CR_OUT_OF_MEMORY;
            break;
        }

        cr = CM_Get_Device_Interface_List((LPGUID)&GUID_DEVINTERFACE_VOLUME,
                                          NULL,
                                          DeviceInterfaceList,
                                          DeviceInterfaceListLength,
                                          CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES);
    } while (cr == CR_BUFFER_SMALL);

    if (cr != CR_SUCCESS)
    {
        goto Exit;
    }

```






> [!NOTE]
> The cfgmgr32.h header defines CM_Get_Device_Interface_List as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea">CM_Get_Device_Interface_List_Size</a>
