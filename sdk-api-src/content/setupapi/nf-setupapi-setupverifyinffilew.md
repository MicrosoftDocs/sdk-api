---
UID: NF:setupapi.SetupVerifyInfFileW
title: SetupVerifyInfFileW function
author: windows-sdk-content
description: The SetupVerifyInfFile function verifies the digital signature of the specified INF file by using its corresponding catalog. The verification can be performed against an alternate platform.
old-location: setup\setupverifyinffile.htm
old-project: SetupApi
ms.assetid: 3e64783f-6ded-498a-a994-ccd3ba217e91
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: SetupVerifyInfFile, SetupVerifyInfFile function [Setup API], SetupVerifyInfFileA, SetupVerifyInfFileW, _setupapi_setupverifyinffile, setup.setupverifyinffile, setupapi/SetupVerifyInfFile, setupapi/SetupVerifyInfFileA, setupapi/SetupVerifyInfFileW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
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
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupVerifyInfFileW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupVerifyInfFile</b> function verifies the digital signature of the specified INF file by using its corresponding catalog. The verification can be performed against an alternate platform.


## -parameters




### -param InfName [in]

The name of the INF file to be verified. This name may include a path.


### -param AltPlatformInfo [in]

An optional pointer to a 
<a href="https://msdn.microsoft.com/eb66ef5a-212d-4224-87b5-d64e8e188139">SP_ALTPLATFORM_INFO_V2</a> structure that contains information about the alternate platform to use when validating the INF file. This parameter can be Null.


### -param InfSignerInfo

TBD




#### - InfFileName [out]

A pointer to an <a href="https://msdn.microsoft.com/50ceee47-3a89-4bd7-8508-5a4d75514861">SP_INF_SIGNER_INFO</a> structure that receives information about the INF digital signature, that is, if it is signed.


## -returns



This function returns WINSETUPAPI BOOL.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

