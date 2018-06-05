---
UID: NF:cfgmgr32.CM_Get_Device_ID_List_SizeA
title: CM_Get_Device_ID_List_SizeA function
author: windows-sdk-content
description: The CM_Get_Device_ID_List_Size function retrieves the buffer size required to hold a list of device instance IDs for the local machine's device instances.
old-location: devinst\cm_get_device_id_list_size.htm
old-project: devinst
ms.assetid: 3c650b21-56dc-4ef5-b986-417a247b3eb0
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: CM_Get_Device_ID_List_Size, CM_Get_Device_ID_List_Size function [Device and Driver Installation], CM_Get_Device_ID_List_SizeA, CM_Get_Device_ID_List_SizeW, cfgmgr32/CM_Get_Device_ID_List_Size, cfgmgr32/CM_Get_Device_ID_List_SizeA, cfgmgr32/CM_Get_Device_ID_List_SizeW, cfgmgrfn_b3d09a40-04c8-4b59-9e33-cd8b7a41972d.xml, devinst.cm_get_device_id_list_size
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_ID_List_SizeW (Unicode) and CM_Get_Device_ID_List_SizeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CfgMgr32.dll
-	API-MS-Win-Devices-Config-L1-1-0.dll
-	API-MS-Win-Devices-Config-L1-1-1.dll
api_name:
-	CM_Get_Device_ID_List_Size
-	CM_Get_Device_ID_List_SizeA
-	CM_Get_Device_ID_List_SizeW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
---

# CM_Get_Device_ID_List_SizeA function


## -description


The <b>CM_Get_Device_ID_List_Size</b> function retrieves the buffer size required to hold a list of <a href="devinst.device_instance_ids">device instance IDs</a> for the local machine's <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instances</a>.


## -parameters




### -param pulLen [out]

Receives a value representing the required buffer size, in characters.


### -param pszFilter [in, optional]

Caller-supplied pointer to a character string specifying a subset of the machine's device instance identifiers, or <b>NULL</b>. See the following description of <i>ulFlags</i>.


### -param ulFlags [in]

One of the optional, caller-supplied bit flags that specify search filters. If no flags are specified, the function supplies the buffer size required to hold all instance identifiers for all device instances. For a list of bit flags, see the <i>ulFlags</i> description for <a href="https://msdn.microsoft.com/library/windows/hardware/ff538415">CM_Get_Device_ID_List</a>.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The <b>CM_Get_Device_ID_List_Size</b> function should be called to determine the buffer size required by <a href="https://msdn.microsoft.com/library/windows/hardware/ff538415">CM_Get_Device_ID_List</a>.

The size value supplied in the location pointed to by <i>pulLen</i> is guaranteed to represent a buffer size large enough to hold all device instance identifier strings and terminating NULLs. The supplied value might actually represent a buffer size that is larger than necessary, so don't assume the value represents the true length of the character strings that <a href="https://msdn.microsoft.com/library/windows/hardware/ff538415">CM_Get_Device_ID_List</a> will provide.

For information about device instance IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538433">CM_Get_Device_ID_List_Size_Ex</a>
 

 

