---
UID: NF:cfgmgr32.CM_Get_Device_ID_List_Size_ExA
tech.root: devinst 
title: CM_Get_Device_ID_List_Size_ExA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Get_Device_ID_List_Size_Ex function retrieves the buffer size required to hold a list of device instance IDs for a local or a remote machine's device instances. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cfgmgr32.h
req.idl: 
req.include-header: Cfgmgr32.h 
req.irql: 
req.kmdf-ver: 
req.lib: Cfgmgr32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows. 
req.target-min-winversvr: 
req.target-type: Desktop 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport 
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Get_Device_ID_List_Size_ExA
 - CM_Get_Device_ID_List_Size_Ex
f1_keywords:
 - CM_Get_Device_ID_List_Size_ExA
 - cfgmgr32/CM_Get_Device_ID_List_Size_ExA
 - CM_Get_Device_ID_List_Size_Ex
 - cfgmgr32/CM_Get_Device_ID_List_Size_Ex
dev_langs:
 - c++
---

# CM_Get_Device_ID_List_Size_ExA function

## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea">CM_Get_Device_ID_List_Size</a> instead.]

The <b>CM_Get_Device_ID_List_Size_Ex</b> function retrieves the buffer size required to hold a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for a local or a remote machine's <a href="/windows-hardware/drivers/">device instances</a>.

## -parameters

### -param pulLen [out]

Receives a value representing the required buffer size, in characters.

### -param pszFilter [in, optional]

Caller-supplied pointer to a character string specifying a subset of the machine's device instance identifiers, or <b>NULL</b>. See the following description of <i>ulFlags</i>.

### -param ulFlags [in]

One of the optional, caller-supplied bit flags that specify search filters. If no flags are specified, the function supplies the buffer size required to hold all instance identifiers for all device instances. For a list of bit flags, see the <i>ulFlags</i> description for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exa">CM_Get_Device_ID_List_Ex</a>.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinea">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The <b>CM_Get_Device_ID_List_Size_Ex</b> function should be called to determine the buffer size required by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exa">CM_Get_Device_ID_List_Ex</a>.

The size value supplied in the location pointed to by <i>pulLen</i> is guaranteed to represent a buffer size large enough to hold all device instance identifier strings and terminating NULLs. The supplied value might actually represent a buffer size that is larger than necessary, so don't assume the value represents the true length of the character strings that <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exa">CM_Get_Device_ID_List_Ex</a> will provide.

For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea">CM_Get_Device_ID_List_Size</a>
