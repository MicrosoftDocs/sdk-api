---
UID: NF:cfgmgr32.CM_Get_Device_ID_List_ExA
tech.root: devinst 
title: CM_Get_Device_ID_List_ExA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Get_Device_ID_List_Ex function retrieves a list of device instance IDs for the device instances on a local or a remote machine. (ANSI)
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
 - CM_Get_Device_ID_List_ExA
 - CM_Get_Device_ID_List_Ex
f1_keywords:
 - CM_Get_Device_ID_List_ExA
 - cfgmgr32/CM_Get_Device_ID_List_ExA
 - CM_Get_Device_ID_List_Ex
 - cfgmgr32/CM_Get_Device_ID_List_Ex
dev_langs:
 - c++
---

# CM_Get_Device_ID_List_ExA function

## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a> instead.]

The <b>CM_Get_Device_ID_List_Ex</b> function retrieves a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the <a href="/windows-hardware/drivers/">device instances</a> on a local or a remote machine.

## -parameters

### -param pszFilter [in, optional]

Caller-supplied pointer to a character string specifying a subset of the machine's device instance identifiers, or <b>NULL</b>. See the following description of <i>ulFlags</i>.

### -param Buffer [out]

Address of a buffer to receive a set of NULL-terminated device instance identifier strings. The end of the set is terminated by an extra <b>NULL</b>. The required buffer size should be obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exa">CM_Get_Device_ID_List_Size_Ex</a>.

### -param BufferLen [in]

Caller-supplied length, in characters, of the buffer specified by <i>Buffer</i>.

### -param ulFlags [in]

One of the optional, caller-supplied bit flags that specify search filters. If no flags are specified, the function supplies all instance identifiers for all device instances. For a list of bit flags, see the <i>ulFlags</i> description for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a>.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinea">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.
