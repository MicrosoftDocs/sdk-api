---
UID: NF:cfgmgr32.CM_Get_Device_ID_Size
title: CM_Get_Device_ID_Size function
author: windows-sdk-content
description: The CM_Get_Device_ID_Size function retrieves the buffer size required to hold a device instance ID for a device instance on the local machine.
old-location: devinst\cm_get_device_id_size.htm
tech.root: devinst
ms.assetid: 3ae682d0-d9fa-4a29-8258-c6f72f1940b7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CM_Get_Device_ID_Size, CM_Get_Device_ID_Size function [Device and Driver Installation], cfgmgr32/CM_Get_Device_ID_Size, cfgmgrfn_7e0a024a-355c-4c4d-8aa2-9ec4078c3a3a.xml, devinst.cm_get_device_id_size
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib; OneCoreUAP.lib on Windows 10
req.dll: CfgMgr32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CfgMgr32.dll
 - API-MS-Win-devices-config-l1-1-0.dll
 - API-MS-Win-devices-config-l1-1-1.dll
api_name:
 - CM_Get_Device_ID_Size
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CM_Get_Device_ID_Size
: 
---

# CM_Get_Device_ID_Size function


## -description


The <b>CM_Get_Device_ID_Size</b> function retrieves the buffer size required to hold a <a href="devinst.device_instance_ids">device instance ID</a> for a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instance</a> on the local machine.


## -parameters




### -param pulLen [out]

Receives a value representing the required buffer size, in characters.


### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the local machine.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The <b>CM_Get_Device_ID_Size</b> function should be called to determine the buffer size required by <a href="https://msdn.microsoft.com/924906ca-1119-428f-a42d-cb9a784af011">CM_Get_Device_ID</a>.

The size value supplied in the location pointed to by <i>pulLen</i> is less than MAX_DEVICE_ID_LEN, and does not include the identifier string's terminating <b>NULL</b>. If the specified device instance does not exist, the function supplies a size value of zero.

For information about device instance IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

For information about using device instance handles that are bound to the local machine, see <a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>.




## -see-also




<a href="https://msdn.microsoft.com/b339d794-cbf0-46aa-a106-b2837f797def">CM_Get_Child</a>



<a href="https://msdn.microsoft.com/924906ca-1119-428f-a42d-cb9a784af011">CM_Get_Device_ID</a>



<a href="https://msdn.microsoft.com/3b95f8e3-0059-4a2e-8c14-5938f5826faf">CM_Get_Device_ID_Size_Ex</a>
 

 

