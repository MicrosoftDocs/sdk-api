---
UID: NF:cfgmgr32.CM_Get_Device_ID_ExA
tech.root: devinst 
title: CM_Get_Device_ID_ExA
ms.date: 04/12/2021
targetos: Windows
description: The CM_Get_Device_ID_Ex function retrieves the device instance ID for a specified device instance on a local or a remote machine. (ANSI)
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
 - CM_Get_Device_ID_ExA
 - CM_Get_Device_ID_Ex
f1_keywords:
 - CM_Get_Device_ID_ExA
 - cfgmgr32/CM_Get_Device_ID_ExA
 - CM_Get_Device_ID_Ex
 - cfgmgr32/CM_Get_Device_ID_Ex
dev_langs:
 - c++
---

# CM_Get_Device_ID_ExA function

## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_ida">CM_Get_Device_ID</a> instead.]

The <b>CM_Get_Device_ID_Ex</b> function retrieves the <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> for a specified <a href="/windows-hardware/drivers/">device instance</a> on a local or a remote machine.

## -parameters

### -param dnDevInst [in]

Caller-supplied device instance handle that is bound to the machine handle supplied by <i>hMachine</i>.

### -param Buffer [out]

Address of a buffer to receive a device instance ID string. The required buffer size can be obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex">CM_Get_Device_ID_Size_Ex</a>, then incrementing the received value to allow room for the string's terminating <b>NULL</b>.

### -param BufferLen [in]

Caller-supplied length, in characters, of the buffer specified by <i>Buffer</i>.

### -param ulFlags

Not used, must be zero.

### -param hMachine [in, optional]

Caller-supplied machine handle to which the caller-supplied device instance handle is bound.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The function appends a NULL terminator to the supplied <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> string, unless the buffer is too small to hold the string. In this case, the function supplies as much of the identifier string as will fit into the buffer, and then returns CR_BUFFER_SMALL.

For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

For information about using device instance handles that are bound to a local or a remote machine, see <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>.

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_child_ex">CM_Get_Child_Ex</a>  
<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_ida">CM_Get_Device_ID</a>  
