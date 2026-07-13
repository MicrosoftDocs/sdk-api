---
UID: NF:cfgmgr32.CM_Get_Device_ID_List_SizeW
title: CM_Get_Device_ID_List_SizeW function (cfgmgr32.h)
description: The CM_Get_Device_ID_List_Size function retrieves the buffer size required to hold a list of device instance IDs for the local machine's device instances. (Unicode)
helpviewer_keywords: ["CM_Get_Device_ID_List_Size", "CM_Get_Device_ID_List_Size function [Device and Driver Installation]", "CM_Get_Device_ID_List_SizeW", "cfgmgr32/CM_Get_Device_ID_List_Size", "cfgmgr32/CM_Get_Device_ID_List_SizeW", "cfgmgrfn_b3d09a40-04c8-4b59-9e33-cd8b7a41972d.xml", "devinst.cm_get_device_id_list_size"]
old-location: devinst\cm_get_device_id_list_size.htm
tech.root: devinst
ms.assetid: 3c650b21-56dc-4ef5-b986-417a247b3eb0
ms.date: 12/05/2018
ms.keywords: CM_Get_Device_ID_List_Size, CM_Get_Device_ID_List_Size function [Device and Driver Installation], CM_Get_Device_ID_List_SizeA, CM_Get_Device_ID_List_SizeW, cfgmgr32/CM_Get_Device_ID_List_Size, cfgmgr32/CM_Get_Device_ID_List_SizeA, cfgmgr32/CM_Get_Device_ID_List_SizeW, cfgmgrfn_b3d09a40-04c8-4b59-9e33-cd8b7a41972d.xml, devinst.cm_get_device_id_list_size
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
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Device_ID_List_SizeW
 - cfgmgr32/CM_Get_Device_ID_List_SizeW
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
 - CM_Get_Device_ID_List_Size
 - CM_Get_Device_ID_List_SizeA
 - CM_Get_Device_ID_List_SizeW
---

# CM_Get_Device_ID_List_SizeW function


## -description

The <b>CM_Get_Device_ID_List_Size</b> function retrieves the buffer size required to hold a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the local machine's <a href="/windows-hardware/drivers/">device instances</a>.

## -parameters

### -param pulLen [out]

Receives a value representing the required buffer size, in characters.

### -param pszFilter [in, optional]

Caller-supplied pointer to a character string specifying a subset of the machine's device instance identifiers, or <b>NULL</b>. See the following description of <i>ulFlags</i>.

### -param ulFlags [in]

One of the optional, caller-supplied bit flags that specify search filters. If no flags are specified, the function supplies the buffer size required to hold all instance identifiers for all device instances. For a list of bit flags, see the <i>ulFlags</i> description for <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a>.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

The <b>CM_Get_Device_ID_List_Size</b> function should be called to determine the buffer size required by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a>.

The size value supplied in the location pointed to by <i>pulLen</i> is guaranteed to represent a buffer size large enough to hold all device instance identifier strings and terminating NULLs. The supplied value might actually represent a buffer size that is larger than necessary, so don't assume the value represents the true length of the character strings that <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista">CM_Get_Device_ID_List</a> will provide.

For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.





> [!NOTE]
> The cfgmgr32.h header defines CM_Get_Device_ID_List_Size as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw">CM_Get_Device_ID_List_Size_Ex</a>
