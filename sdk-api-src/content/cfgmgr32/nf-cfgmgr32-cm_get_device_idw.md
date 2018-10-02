---
UID: NF:cfgmgr32.CM_Get_Device_IDW
title: CM_Get_Device_IDW function
author: windows-sdk-content
description: The CM_Get_Device_ID function retrieves the device instance ID for a specified device instance on the local machine.
old-location: devinst\cm_get_device_id.htm
tech.root: devinst
ms.assetid: 924906ca-1119-428f-a42d-cb9a784af011
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CM_Get_Device_ID, CM_Get_Device_ID function [Device and Driver Installation], CM_Get_Device_IDW, cfgmgr32/CM_Get_Device_ID, cfgmgr32/CM_Get_Device_IDW, cfgmgrfn_9b900d97-f812-412b-b12c-d64b9aba3be7.xml, devinst.cm_get_device_id
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_IDW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
 - API-Ms-Win-Devices-Config-L1-1-0.dll
 - API-Ms-Win-Devices-Config-L1-1-1.dll
 - CfgMgr32.dll
api_name:
 - CM_Get_Device_ID
 - CM_Get_Device_IDW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_Device_IDW function


## -description


The <b>CM_Get_Device_ID</b> function retrieves the <a href="devinst.device_instance_ids">device instance ID</a> for a specified <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instance</a> on the local machine.


## -parameters




### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param Buffer [out]

Address of a buffer to receive a device instance ID string. The required buffer size can be obtained by calling <a href="https://msdn.microsoft.com/3ae682d0-d9fa-4a29-8258-c6f72f1940b7">CM_Get_Device_ID_Size</a>, then incrementing the received value to allow room for the string's terminating <b>NULL</b>. 


### -param BufferLen [in]

Caller-supplied length, in characters, of the buffer specified by <i>Buffer</i>.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The function appends a NULL terminator to the supplied device instance ID string, unless the buffer is too small to hold the string. In this case, the function supplies as much of the identifier string as will fit into the buffer, and then returns CR_BUFFER_SMALL. 

For information about device instance IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/757b8185-c5f5-4623-a410-63fd2f74e34f">CM_Get_Device_ID_Ex</a>
 

 

