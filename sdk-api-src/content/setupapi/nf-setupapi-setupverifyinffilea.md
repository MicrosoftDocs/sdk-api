---
UID: NF:setupapi.SetupVerifyInfFileA
title: SetupVerifyInfFileA function (setupapi.h)
description: The SetupVerifyInfFile function verifies the digital signature of the specified INF file by using its corresponding catalog. The verification can be performed against an alternate platform.
helpviewer_keywords: ["SetupVerifyInfFile","SetupVerifyInfFile function [Setup API]","SetupVerifyInfFileA","SetupVerifyInfFileW","_setupapi_setupverifyinffile","setup.setupverifyinffile","setupapi/SetupVerifyInfFile","setupapi/SetupVerifyInfFileA","setupapi/SetupVerifyInfFileW"]
old-location: setup\setupverifyinffile.htm
tech.root: SetupApi
ms.assetid: 3e64783f-6ded-498a-a994-ccd3ba217e91
ms.date: 12/05/2018
ms.keywords: SetupVerifyInfFile, SetupVerifyInfFile function [Setup API], SetupVerifyInfFileA, SetupVerifyInfFileW, _setupapi_setupverifyinffile, setup.setupverifyinffile, setupapi/SetupVerifyInfFile, setupapi/SetupVerifyInfFileA, setupapi/SetupVerifyInfFileW
f1_keywords:
- setupapi/SetupVerifyInfFile
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO_V2</a> structure that contains information about the alternate platform to use when validating the INF file. This parameter can be Null.


### -param InfSignerInfo [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_inf_signer_info_v1_a">SP_INF_SIGNER_INFO</a> structure that receives information about the INF digital signature, that is, if it is signed.


## -returns



This function returns WINSETUPAPI BOOL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>
 

 

