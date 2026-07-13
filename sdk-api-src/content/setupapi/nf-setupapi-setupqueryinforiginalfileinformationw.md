---
UID: NF:setupapi.SetupQueryInfOriginalFileInformationW
title: SetupQueryInfOriginalFileInformationW function (setupapi.h)
description: The SetupQueryInfOriginalFileInformation function returns the original name of an OEM INF file. (Unicode)
helpviewer_keywords: ["SetupQueryInfOriginalFileInformation", "SetupQueryInfOriginalFileInformation function [Setup API]", "SetupQueryInfOriginalFileInformationW", "_setupapi_setupqueryinforiginalfileinformation", "setup.setupqueryinforiginalfileinformation", "setupapi/SetupQueryInfOriginalFileInformation", "setupapi/SetupQueryInfOriginalFileInformationW"]
old-location: setup\setupqueryinforiginalfileinformation.htm
tech.root: setup
ms.assetid: bc7c08ff-3d6b-4d45-b634-1358302f6fc6
ms.date: 12/05/2018
ms.keywords: SetupQueryInfOriginalFileInformation, SetupQueryInfOriginalFileInformation function [Setup API], SetupQueryInfOriginalFileInformationA, SetupQueryInfOriginalFileInformationW, _setupapi_setupqueryinforiginalfileinformation, setup.setupqueryinforiginalfileinformation, setupapi/SetupQueryInfOriginalFileInformation, setupapi/SetupQueryInfOriginalFileInformationA, setupapi/SetupQueryInfOriginalFileInformationW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupQueryInfOriginalFileInformationW (Unicode) and SetupQueryInfOriginalFileInformationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupQueryInfOriginalFileInformationW
 - setupapi/SetupQueryInfOriginalFileInformationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupQueryInfOriginalFileInformation
 - SetupQueryInfOriginalFileInformationA
 - SetupQueryInfOriginalFileInformationW
---

# SetupQueryInfOriginalFileInformationW function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueryInfOriginalFileInformation</b> function returns the original name of an OEM INF file.

## -parameters

### -param InfInformation [in]

Pointer to an 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_inf_information">SP_INF_INFORMATION</a> structure returned from a call to the 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfinformationa">SetupGetInfInformation</a> function.

### -param InfIndex [in]

Index of the constituent INF file name to retrieve. This index can be in the range [0, <i>InfInformation.InfCount</i>). Meaning that the values zero through, but not including, <i>InfInformation.InfCount</i> are valid.

### -param AlternatePlatformInfo [in]

Optional pointer to an 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v1">SP_ALTPLATFORM_INFO_V1</a> or <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO_V2</a> structure used to pass information for an alternate platform to 
<b>SetupQueryInfOriginalFileInformation</b>.

### -param OriginalFileInfo [out]

Pointer to an 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_original_file_info_a">SP_ORIGINAL_FILE_INFO</a> structure that receives the original INF file name and catalog file information returned by 
<b>SetupQueryInfOriginalFileInformation</b>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupQueryInfOriginalFileInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
