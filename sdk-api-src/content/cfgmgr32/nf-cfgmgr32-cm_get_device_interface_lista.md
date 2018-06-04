---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CM_Get_Device_Interface_ListA function


## -description


The <b>CM_Get_Device_Interface_List</b> function retrieves a list of device interface instances that belong to a specified <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a>.


## -parameters




### -param InterfaceClassGuid [in]

Supplies a GUID that identifies a device interface class.


### -param pDeviceID [in, optional]

Caller-supplied pointer to a NULL-terminated string that represents a <a href="devinst.device_instance_ids">device instance ID</a>. If specified, the function retrieves device interfaces that are supported by the device for the specified class. If this value is <b>NULL</b>, or if it points to a zero-length string, the function retrieves all interfaces that belong to the specified class.


### -param Buffer [out]

Caller-supplied pointer to a buffer that receives multiple, NULL-terminated Unicode strings, each representing the symbolic link name of an interface instance.


### -param BufferLen [in]

Caller-supplied value that specifies the length, in characters, of the buffer pointed to by <i>Buffer</i>. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538471">CM_Get_Device_Interface_List_Size</a> to determine the required buffer size.


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




        
      Between calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff538471">CM_Get_Device_Interface_List_Size</a> to get the size of the list and calling <b>CM_Get_Device_Interface_List</b> to get the list, a new device interface can be added to the system causing the size returned to no longer be valid.  Callers should be robust to that condition and retry getting the size and the list if <b>CM_Get_Device_Interface_List</b> returns <b>CR_BUFFER_SMALL</b>.


#### Examples

This snippet illustrates retrying getting the size and the list as described in the Remarks section.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>    CONFIGRET cr = CR_SUCCESS;
    PWSTR DeviceInterfaceList = NULL;
    ULONG DeviceInterfaceListLength = 0;

    do {
        cr = CM_Get_Device_Interface_List_Size(&amp;DeviceInterfaceListLength,
                                               (LPGUID)&amp;GUID_DEVINTERFACE_VOLUME,
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

        cr = CM_Get_Device_Interface_List((LPGUID)&amp;GUID_DEVINTERFACE_VOLUME,
                                          NULL,
                                          DeviceInterfaceList,
                                          DeviceInterfaceListLength,
                                          CM_GET_DEVICE_INTERFACE_LIST_ALL_DEVICES);
    } while (cr == CR_BUFFER_SMALL);

    if (cr != CR_SUCCESS)
    {
        goto Exit;
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538471">CM_Get_Device_Interface_List_Size</a>
 

 

