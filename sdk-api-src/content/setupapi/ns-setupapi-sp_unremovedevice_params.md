---
UID: NS:setupapi._SP_UNREMOVEDEVICE_PARAMS
title: SP_UNREMOVEDEVICE_PARAMS (setupapi.h)
description: An SP_UNREMOVEDEVICE_PARAMS structure corresponds to a DIF_UNREMOVE installation request.
helpviewer_keywords: ["*PSP_UNREMOVEDEVICE_PARAMS","PSP_UNREMOVEDEVICE_PARAMS","PSP_UNREMOVEDEVICE_PARAMS structure pointer [Device and Driver Installation]","SP_UNREMOVEDEVICE_PARAMS","SP_UNREMOVEDEVICE_PARAMS structure [Device and Driver Installation]","devinst.sp_unremovedevice_params","di-struct_bcd98087-c502-40d6-81a7-5154340ce406.xml","setupapi/PSP_UNREMOVEDEVICE_PARAMS","setupapi/SP_UNREMOVEDEVICE_PARAMS"]
old-location: devinst\sp_unremovedevice_params.htm
tech.root: devinst
ms.assetid: 89f5e2a9-5336-421f-b781-688588695027
ms.date: 12/05/2018
ms.keywords: '*PSP_UNREMOVEDEVICE_PARAMS, PSP_UNREMOVEDEVICE_PARAMS, PSP_UNREMOVEDEVICE_PARAMS structure pointer [Device and Driver Installation], SP_UNREMOVEDEVICE_PARAMS, SP_UNREMOVEDEVICE_PARAMS structure [Device and Driver Installation], devinst.sp_unremovedevice_params, di-struct_bcd98087-c502-40d6-81a7-5154340ce406.xml, setupapi/PSP_UNREMOVEDEVICE_PARAMS, setupapi/SP_UNREMOVEDEVICE_PARAMS'
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
req.typenames: SP_UNREMOVEDEVICE_PARAMS, *PSP_UNREMOVEDEVICE_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_UNREMOVEDEVICE_PARAMS
 - setupapi/_SP_UNREMOVEDEVICE_PARAMS
 - PSP_UNREMOVEDEVICE_PARAMS
 - setupapi/PSP_UNREMOVEDEVICE_PARAMS
 - SP_UNREMOVEDEVICE_PARAMS
 - setupapi/SP_UNREMOVEDEVICE_PARAMS
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
 - SP_UNREMOVEDEVICE_PARAMS
---

# SP_UNREMOVEDEVICE_PARAMS structure


## -description

An SP_UNREMOVEDEVICE_PARAMS structure corresponds to a DIF_UNREMOVE installation request.

## -struct-fields

### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>.

### -field Scope

A flag that indicates the scope of the unremove operation. This flag must always be set to DI_UNREMOVEDEVICE_CONFIGSPECIFIC.

### -field HwProfile

The hardware profile ID for profile-specific changes. Zero specifies the current hardware profile.

## -see-also

<a href="/windows-hardware/drivers/install/dif-unremove">DIF_UNREMOVE</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiunremovedevice">SetupDiUnremoveDevice</a>