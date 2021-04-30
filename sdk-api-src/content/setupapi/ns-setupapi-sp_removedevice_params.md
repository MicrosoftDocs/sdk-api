---
UID: NS:setupapi._SP_REMOVEDEVICE_PARAMS
title: SP_REMOVEDEVICE_PARAMS (setupapi.h)
description: An SP_REMOVEDEVICE_PARAMS structure corresponds to the DIF_REMOVE installation request.
helpviewer_keywords: ["*PSP_REMOVEDEVICE_PARAMS","PSP_REMOVEDEVICE_PARAMS","PSP_REMOVEDEVICE_PARAMS structure pointer [Device and Driver Installation]","SP_REMOVEDEVICE_PARAMS","SP_REMOVEDEVICE_PARAMS structure [Device and Driver Installation]","devinst.sp_removedevice_params","di-struct_a1c87aad-2f81-4545-a088-1dadc98372d7.xml","setupapi/PSP_REMOVEDEVICE_PARAMS","setupapi/SP_REMOVEDEVICE_PARAMS"]
old-location: devinst\sp_removedevice_params.htm
tech.root: devinst
ms.assetid: 08d3a5c7-9350-4fb3-8476-fb22e34d7054
ms.date: 12/05/2018
ms.keywords: '*PSP_REMOVEDEVICE_PARAMS, PSP_REMOVEDEVICE_PARAMS, PSP_REMOVEDEVICE_PARAMS structure pointer [Device and Driver Installation], SP_REMOVEDEVICE_PARAMS, SP_REMOVEDEVICE_PARAMS structure [Device and Driver Installation], devinst.sp_removedevice_params, di-struct_a1c87aad-2f81-4545-a088-1dadc98372d7.xml, setupapi/PSP_REMOVEDEVICE_PARAMS, setupapi/SP_REMOVEDEVICE_PARAMS'
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_REMOVEDEVICE_PARAMS, *PSP_REMOVEDEVICE_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_REMOVEDEVICE_PARAMS
 - setupapi/_SP_REMOVEDEVICE_PARAMS
 - PSP_REMOVEDEVICE_PARAMS
 - setupapi/PSP_REMOVEDEVICE_PARAMS
 - SP_REMOVEDEVICE_PARAMS
 - setupapi/SP_REMOVEDEVICE_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_REMOVEDEVICE_PARAMS
---

# SP_REMOVEDEVICE_PARAMS structure


## -description

An SP_REMOVEDEVICE_PARAMS structure corresponds to the <a href="/windows-hardware/drivers/install/dif-remove">DIF_REMOVE</a> installation request.

## -struct-fields

### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>.

### -field Scope

Flags that indicate the scope of the device removal. Can be one of the following values:





#### DI_REMOVEDEVICE_GLOBAL

Make this change in all hardware profiles. Remove information about the device from the registry.



#### DI_REMOVEDEVICE_CONFIGSPECIFIC

Make this change to only the hardware profile specified by <b>HwProfile</b>. this flag only applies to root-enumerated devices. When Windows removes the device from the last hardware profile in which it was configured, Windows performs a global removal.

### -field HwProfile

The hardware profile ID for profile-specific changes. Zero specifies the current hardware profile.

## -see-also

<a href="/windows-hardware/drivers/install/dif-remove">DIF_REMOVE</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiremovedevice">SetupDiRemoveDevice</a>