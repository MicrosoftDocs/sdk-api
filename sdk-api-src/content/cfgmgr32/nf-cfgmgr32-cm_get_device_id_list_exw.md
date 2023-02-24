---
UID: NF:cfgmgr32.CM_Get_Device_ID_List_ExW
title: CM_Get_Device_ID_List_ExW function (cfgmgr32.h)
description: The CM_Get_Device_ID_List_Ex function retrieves a list of device instance IDs for the device instances on a local or a remote machine. (Unicode)
helpviewer_keywords: ["CM_Get_Device_ID_List_Ex", "CM_Get_Device_ID_List_Ex function [Device and Driver Installation]", "CM_Get_Device_ID_List_ExW", "cfgmgr32/CM_Get_Device_ID_List_Ex", "cfgmgr32/CM_Get_Device_ID_List_ExW", "cfgmgrfn_85ea1296-d9ef-46fd-8893-b44cd188ed6f.xml", "devinst.cm_get_device_id_list_ex"]
old-location: devinst\cm_get_device_id_list_ex.htm
tech.root: devinst
ms.assetid: 4f47e44c-a30b-4d50-9041-f84f7f209764
ms.date: 12/05/2018
ms.keywords: CM_Get_Device_ID_List_Ex, CM_Get_Device_ID_List_Ex function [Device and Driver Installation], CM_Get_Device_ID_List_ExW, cfgmgr32/CM_Get_Device_ID_List_Ex, cfgmgr32/CM_Get_Device_ID_List_ExW, cfgmgrfn_85ea1296-d9ef-46fd-8893-b44cd188ed6f.xml, devinst.cm_get_device_id_list_ex
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_ID_List_ExW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Device_ID_List_ExW
 - cfgmgr32/CM_Get_Device_ID_List_ExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Get_Device_ID_List_Ex
 - CM_Get_Device_ID_List_ExW
---

# CM_Get_Device_ID_List_ExW function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a> instead.]

The <b>CM_Get_Device_ID_List_Ex</b> function retrieves a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the <a href="/windows-hardware/drivers/">device instances</a> on a local or a remote machine.

## -parameters

### -param pszFilter [in, optional]

Caller-supplied pointer to a character string specifying a subset of the machine's device instance identifiers, or <b>NULL</b>. See the following description of <i>ulFlags</i>.

### -param Buffer [out]

Address of a buffer to receive a set of NULL-terminated device instance identifier strings. The end of the set is terminated by an extra <b>NULL</b>. The required buffer size should be obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw">CM_Get_Device_ID_List_Size_Ex</a>.

### -param BufferLen [in]

Caller-supplied length, in characters, of the buffer specified by <i>Buffer</i>.

### -param ulFlags [in]

One of the optional, caller-supplied bit flags that specify search filters. If no flags are specified, the function supplies all instance identifiers for all device instances. For a list of bit flags, see the <i>ulFlags</i> description for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a>.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.
