---
UID: NF:setupapi.SetupVerifyInfFileA
title: SetupVerifyInfFileA function (setupapi.h)
description: The SetupVerifyInfFile function verifies the digital signature of the specified INF file by using its corresponding catalog. The verification can be performed against an alternate platform. (ANSI)
helpviewer_keywords: ["SetupVerifyInfFileA", "setupapi/SetupVerifyInfFileA"]
old-location: setup\setupverifyinffile.htm
tech.root: setup
ms.assetid: 3e64783f-6ded-498a-a994-ccd3ba217e91
ms.date: 12/05/2018
ms.keywords: SetupVerifyInfFile, SetupVerifyInfFile function [Setup API], SetupVerifyInfFileA, SetupVerifyInfFileW, _setupapi_setupverifyinffile, setup.setupverifyinffile, setupapi/SetupVerifyInfFile, setupapi/SetupVerifyInfFileA, setupapi/SetupVerifyInfFileW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupVerifyInfFileW (Unicode) and SetupVerifyInfFileA (ANSI)
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
 - SetupVerifyInfFileA
 - setupapi/SetupVerifyInfFileA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupVerifyInfFile
 - SetupVerifyInfFileA
 - SetupVerifyInfFileW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupVerifyInfFileA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupVerifyInfFile</b> function verifies the digital signature of the specified INF file by using its corresponding catalog. The verification can be performed against an alternate platform.

## -parameters

### -param InfName [in]

The name of the INF file to be verified. This name may include a path.

### -param AltPlatformInfo [in]

An optional pointer to a 
<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO_V2</a> structure that contains information about the alternate platform to use when validating the INF file. This parameter can be Null.

### -param InfSignerInfo [out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_inf_signer_info_v1_a">SP_INF_SIGNER_INFO</a> structure that receives information about the INF digital signature, that is, if it is signed.

## -returns

This function returns WINSETUPAPI BOOL.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupVerifyInfFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
