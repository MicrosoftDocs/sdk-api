---
UID: NF:cfgmgr32.CM_Get_Device_ID_List_Size_ExW
title: CM_Get_Device_ID_List_Size_ExW function
author: windows-sdk-content
description: The CM_Get_Device_ID_List_Size_Ex function retrieves the buffer size required to hold a list of device instance IDs for a local or a remote machine's device instances.
old-location: devinst\cm_get_device_id_list_size_ex.htm
old-project: devinst
ms.assetid: ed89ff61-c92b-4841-9038-3c26d8594aee
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: CM_Get_Device_ID_List_Size_Ex, CM_Get_Device_ID_List_Size_Ex function [Device and Driver Installation], CM_Get_Device_ID_List_Size_ExW, cfgmgr32/CM_Get_Device_ID_List_Size_Ex, cfgmgr32/CM_Get_Device_ID_List_Size_ExW, cfgmgrfn_2e9a6787-1578-48c1-9f3b-5d1ee266f9ac.xml, devinst.cm_get_device_id_list_size_ex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_ID_List_Size_ExW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Get_Device_ID_List_Size_Ex
 - CM_Get_Device_ID_List_Size_ExW
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
---

# CM_Get_Device_ID_List_Size_ExW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/library/windows/hardware/ff538427">CM_Get_Device_ID_List_Size</a> instead.]

The <b>CM_Get_Device_ID_List_Size_Ex</b> function retrieves the buffer size required to hold a list of <a href="devinst.device_instance_ids">device instance IDs</a> for a local or a remote machine's <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instances</a>.


## -parameters




### -param pulLen [out]

Receives a value representing the required buffer size, in characters.


### -param pszFilter [in, optional]

Caller-supplied pointer to a character string specifying a subset of the machine's device instance identifiers, or <b>NULL</b>. See the following description of <i>ulFlags</i>.


### -param ulFlags [in]

One of the optional, caller-supplied bit flags that specify search filters. If no flags are specified, the function supplies the buffer size required to hold all instance identifiers for all device instances. For a list of bit flags, see the <i>ulFlags</i> description for <a href="https://msdn.microsoft.com/library/windows/hardware/ff538420">CM_Get_Device_ID_List_Ex</a>.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The <b>CM_Get_Device_ID_List_Size_Ex</b> function should be called to determine the buffer size required by <a href="https://msdn.microsoft.com/library/windows/hardware/ff538420">CM_Get_Device_ID_List_Ex</a>.

The size value supplied in the location pointed to by <i>pulLen</i> is guaranteed to represent a buffer size large enough to hold all device instance identifier strings and terminating NULLs. The supplied value might actually represent a buffer size that is larger than necessary, so don't assume the value represents the true length of the character strings that <a href="https://msdn.microsoft.com/library/windows/hardware/ff538420">CM_Get_Device_ID_List_Ex</a> will provide.

For information about device instance IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538427">CM_Get_Device_ID_List_Size</a>
 

 

