---
UID: NS:setupapi._SP_CLASSINSTALL_HEADER
title: SP_CLASSINSTALL_HEADER (setupapi.h)
description: An SP_CLASSINSTALL_HEADER is the first member of any class install parameters structure. It contains the device installation request code that defines the format of the rest of the install parameters structure.
helpviewer_keywords: ["*PSP_CLASSINSTALL_HEADER","PSP_CLASSINSTALL_HEADER","PSP_CLASSINSTALL_HEADER structure pointer [Device and Driver Installation]","SP_CLASSINSTALL_HEADER","SP_CLASSINSTALL_HEADER structure [Device and Driver Installation]","devinst.sp_classinstall_header","di-struct_96e0dbc0-fe54-4731-9ec7-0e633b521297.xml","setupapi/PSP_CLASSINSTALL_HEADER","setupapi/SP_CLASSINSTALL_HEADER"]
old-location: devinst\sp_classinstall_header.htm
tech.root: devinst
ms.assetid: 9f76b741-d2a7-484d-94cb-b559b017399d
ms.date: 12/05/2018
ms.keywords: '*PSP_CLASSINSTALL_HEADER, PSP_CLASSINSTALL_HEADER, PSP_CLASSINSTALL_HEADER structure pointer [Device and Driver Installation], SP_CLASSINSTALL_HEADER, SP_CLASSINSTALL_HEADER structure [Device and Driver Installation], devinst.sp_classinstall_header, di-struct_96e0dbc0-fe54-4731-9ec7-0e633b521297.xml, setupapi/PSP_CLASSINSTALL_HEADER, setupapi/SP_CLASSINSTALL_HEADER'
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
req.typenames: SP_CLASSINSTALL_HEADER, *PSP_CLASSINSTALL_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_CLASSINSTALL_HEADER
 - setupapi/_SP_CLASSINSTALL_HEADER
 - PSP_CLASSINSTALL_HEADER
 - setupapi/PSP_CLASSINSTALL_HEADER
 - SP_CLASSINSTALL_HEADER
 - setupapi/SP_CLASSINSTALL_HEADER
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
 - SP_CLASSINSTALL_HEADER
---

# SP_CLASSINSTALL_HEADER structure


## -description

An SP_CLASSINSTALL_HEADER is the first member of any class install parameters structure. It contains the device installation request code that defines the format of the rest of the install parameters structure.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_CLASSINSTALL_HEADER structure.

### -field InstallFunction

The device installation request (DIF code) for the class install parameters structure. 

DIF codes have the format DIF_<i>XXX</i> and are defined in <i>Setupapi.h</i>. See <a href="/windows-hardware/drivers/install/handling-dif-codes">Device Installation Function Codes</a> for a complete description of DIF codes.

## -remarks

When a component allocates a class install parameters structure, it typically initializes the header fields of the structure. Such a component sets the <b>InstallFunction</b> member to the DIF code for the installation request and sets <b>cbSize</b> to the size of the SP_CLASSINSTALL_HEADER structure. For example:


```
SP_REMOVEDEVICE_PARAMS RemoveDeviceParams;
RemoveDeviceParams.ClassInstallHeader.cbSize = sizeof(SP_CLASSINSTALL_HEADER);
RemoveDeviceParams.ClassInstallHeader.InstallFunction = DIF_REMOVE;
```


A component must set the <b>InstallFunction</b> member before passing a class install parameters structure to <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassinstallparamsa">SetupDiSetClassInstallParams</a>. 

However, a component does not have to set this field when passing class install parameters to <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassinstallparamsa">SetupDiGetClassInstallParams</a>. This function sets the <b>InstallFunction</b> member in the structure it passes back to the caller. It sets <b>InstallFunction</b> to the DIF_<i>XXX</i> code for the currently active device installation request.

## -see-also

<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_detectdevice_params">SP_DETECTDEVICE_PARAMS</a>



<a href="/windows-hardware/drivers/install/sp-movedev-params">SP_MOVEDEV_PARAMS</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_newdevicewizard_data">SP_NEWDEVICEWIZARD_DATA</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_powermessagewake_params_a">SP_POWERMESSAGEWAKE_PARAMS</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_propchange_params">SP_PROPCHANGE_PARAMS</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_removedevice_params">SP_REMOVEDEVICE_PARAMS</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_selectdevice_params_a">SP_SELECTDEVICE_PARAMS</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_troubleshooter_params_a">SP_TROUBLESHOOTER_PARAMS</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_unremovedevice_params">SP_UNREMOVEDEVICE_PARAMS</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassinstallparamsa">SetupDiGetClassInstallParams</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassinstallparamsa">SetupDiSetClassInstallParams</a>