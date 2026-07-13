---
UID: NF:cfgmgr32.CM_Delete_Device_Interface_Key_ExA
title: CM_Delete_Device_Interface_Key_ExA function (cfgmgr32.h)
description: The CM_Delete_Device_Interface_Key_ExA function deletes the registry subkey that is used by applications and drivers to store interface-specific information.
helpviewer_keywords: ["CM_Delete_Device_Interface_Key_ExA", "CM_Delete_Device_Interface_Key_ExA function [Device and Driver Installation]", "cfgmgr32/CM_Delete_Device_Interface_Key_ExA", "devinst.cm_delete_device_interface_key_exa"]
old-location: devinst\cm_delete_device_interface_key_exa.htm
tech.root: devinst
ms.assetid: B12C62F7-B6B1-46F6-88B4-78F25A14E8F6
ms.date: 12/05/2018
ms.keywords: CM_Delete_Device_Interface_Key_ExA, CM_Delete_Device_Interface_Key_ExA function [Device and Driver Installation], cfgmgr32/CM_Delete_Device_Interface_Key_ExA, devinst.cm_delete_device_interface_key_exa
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 10 and later versions of Windows.
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
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Delete_Device_Interface_Key_ExA
 - cfgmgr32/CM_Delete_Device_Interface_Key_ExA
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
 - CM_Delete_Device_Interface_Key_ExA
---

# CM_Delete_Device_Interface_Key_ExA function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw">CM_Delete_Device_Interface_Key</a> instead.]

The <b>CM_Delete_Device_Interface_Key_ExA</b> function deletes the registry subkey that is used by applications and drivers to store interface-specific information.

## -parameters

### -param pszDeviceInterface [in]

Pointer to a string that identifies the device interface instance of the registry subkey to delete.

### -param ulFlags [in]

Reserved. Must be set to zero.

### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw">CM_Open_Device_Interface_Key</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinterfaceregkey">SetupDiDeleteDeviceInterfaceRegKey</a>

## -remarks

> [!NOTE]
> The cfgmgr32.h header defines CM_Delete_Device_Interface_Key_Ex as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
