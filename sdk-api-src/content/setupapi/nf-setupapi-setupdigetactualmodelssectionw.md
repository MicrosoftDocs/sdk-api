---
UID: NF:setupapi.SetupDiGetActualModelsSectionW
title: SetupDiGetActualModelsSectionW function (setupapi.h)
description: The SetupDiGetActualModelsSection function retrieves the appropriate decorated INF Models section to use when installing a device from a device INF file. (Unicode)
helpviewer_keywords: ["SetupDiGetActualModelsSection", "SetupDiGetActualModelsSection function [Device and Driver Installation]", "SetupDiGetActualModelsSectionW", "devinst.setupdigetactualmodelssection", "di-rtns_d008a45e-8dbe-4d59-ac12-be4ac28eebcb.xml", "setupapi/SetupDiGetActualModelsSection"]
old-location: devinst\setupdigetactualmodelssection.htm
tech.root: devinst
ms.assetid: 8338989a-ef99-479c-8163-ad8d65eba32b
ms.date: 12/05/2018
ms.keywords: SetupDiGetActualModelsSection, SetupDiGetActualModelsSection function [Device and Driver Installation], SetupDiGetActualModelsSectionA, SetupDiGetActualModelsSectionW, devinst.setupdigetactualmodelssection, di-rtns_d008a45e-8dbe-4d59-ac12-be4ac28eebcb.xml, setupapi/SetupDiGetActualModelsSection
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Server 2003 with Service Pack 1 (SP1) and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetActualModelsSectionW
 - setupapi/SetupDiGetActualModelsSectionW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetActualModelsSection
 - SetupDiGetActualModelsSectionW
---

# SetupDiGetActualModelsSectionW function


## -description

The <b>SetupDiGetActualModelsSection</b> function retrieves the appropriate decorated <a href="/windows-hardware/drivers/install/inf-models-section">INF Models section</a> to use when installing a device from a device INF file.

## -parameters

### -param Context [in]

A pointer to an INF file context that specifies a <i>manufacturer-identifier</i> entry in an <a href="/windows-hardware/drivers/install/inf-manufacturer-section">INF Manufacturer section</a> of an INF file. The <i>manufacturer-identifier</i> entry specifies an INF <i>Models</i> section name and optionally specifies <i>TargetOSVersion</i> decorations for the <i>Models</i> section name. For information about INF files and an INF file context, see the Platform SDK topics on <a href="/windows/win32/setupapi/using-inf-files">using INF files</a> and the <a href="/windows/win32/api/setupapi/ns-setupapi-infcontext">INFCONTEXT structure</a>.

### -param AlternatePlatformInfo [in, optional]

A pointer to an <a href="/windows/win32/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO</a> structure that supplies information about a Windows version and processor architecture. The <b>cbSize</b> member of this structure must be set to <b>sizeof(</b>SP_ALTPLATFORM_INFO_V2<b>)</b>. This parameter is optional and can be set to <b>NULL</b>.

### -param InfSectionWithExt [out, optional]

A pointer to a buffer that receives a string that contains the decorated INF <i>Models</i> section name and a NULL terminator. If <i>AlternatePlatformInfo</i> is not supplied, the decorated INF <i>Models</i> section name applies to the current platform; otherwise the name applies to the specified alternative platform. This parameter is optional and can be set to <b>NULL</b>. If this parameter is <b>NULL</b>, the function returns <b>TRUE</b> and sets <i>RequiredSize</i> to the size, in characters, that is required to return the decorated <i>Models</i> section name and a terminating NULL character.

### -param InfSectionWithExtSize [in]

 The size, in characters, of the <i>DecoratedModelsSection </i> buffer. If <i>DecoratedModelsSection</i> is <b>NULL</b>, this parameter must be set to zero.

### -param RequiredSize [out, optional]

A pointer to a DWORD-type variable that receives the size, in characters, of the <i>DecoratedModelsSection</i> buffer that is required to retrieve the decorated <i>Models</i> section name and a terminating NULL character. This parameter is optional and can be set to <b>NULL</b>.

### -param Reserved

Reserved for internal system use. This parameter must be set to <b>NULL</b>.

## -returns

<b>SetupDiGetActualModelsSection</b> returns <b>TRUE</b> if the operation succeeds. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupDiGetActualModelsSection</b> determines which <i>TargetOSVersion</i> fields in the <i>manufacturer-identifier</i> entry (supplied by <i>Context</i>) apply to the current platform, if <i>AlternatePlatformInfo</i> is not supplied, or to an alternative platform, if alternative platform information is supplied. <b>SetupDiGetActualModelsSection</b> selects the most appropriate platform based on all the <i>TargetOSVersion</i> fields, appends the <i>TargetOSVersion</i> string to the INF <i>Models</i> section name, and returns the decorated INF <i>Models</i> section name to the caller. In a <i>manufacturer-identifier</i> entry, the operating system major version is specified by the <i>OSMajorVersion</i> field and the operating system minor version is specified by the <i>OSMinorVersion</i> field.

For information about retrieving an <a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall section</a> for a device, see <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetactualsectiontoinstalla">SetupDiGetActualSectionToInstall</a>.





> [!NOTE]
> The setupapi.h header defines SetupDiGetActualModelsSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall Section</a>



<a href="/windows/win32/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetactualsectiontoinstalla">SetupDiGetActualSectionToInstall</a>
