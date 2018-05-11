---
UID: NF:setupapi.SetupQueryInfOriginalFileInformationA
title: SetupQueryInfOriginalFileInformationA function
author: windows-driver-content
description: The SetupQueryInfOriginalFileInformation function returns the original name of an OEM INF file.
old-location: setup\setupqueryinforiginalfileinformation.htm
old-project: SetupApi
ms.assetid: bc7c08ff-3d6b-4d45-b634-1358302f6fc6
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupQueryInfOriginalFileInformation, SetupQueryInfOriginalFileInformation function [Setup API], SetupQueryInfOriginalFileInformationA, SetupQueryInfOriginalFileInformationW, _setupapi_setupqueryinforiginalfileinformation, setup.setupqueryinforiginalfileinformation, setupapi/SetupQueryInfOriginalFileInformation, setupapi/SetupQueryInfOriginalFileInformationA, setupapi/SetupQueryInfOriginalFileInformationW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupQueryInfOriginalFileInformation
-	SetupQueryInfOriginalFileInformationA
-	SetupQueryInfOriginalFileInformationW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupQueryInfOriginalFileInformationA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueryInfOriginalFileInformation</b> function returns the original name of an OEM INF file.


## -parameters




### -param InfInformation [in]

Pointer to an 
<a href="https://msdn.microsoft.com/1fb08456-bc84-41a1-9f02-8fb499801831">SP_INF_INFORMATION</a> structure returned from a call to the 
<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a> function.


### -param InfIndex [in]

Index of the constituent INF file name to retrieve. This index can be in the range [0, <i>InfInformation.InfCount</i>). Meaning that the values zero through, but not including, <i>InfInformation.InfCount</i> are valid.


### -param AlternatePlatformInfo [in]

Optional pointer to an 
<a href="https://msdn.microsoft.com/33872a84-8f7f-4508-a326-2d95ac0fcfd7">SP_ALTPLATFORM_INFO_V1</a> or <a href="https://msdn.microsoft.com/eb66ef5a-212d-4224-87b5-d64e8e188139">SP_ALTPLATFORM_INFO_V2</a> structure used to pass information for an alternate platform to 
<b>SetupQueryInfOriginalFileInformation</b>.


### -param OriginalFileInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/9ce09717-7f01-4044-ad6b-edd04a2445f5">SP_ORIGINAL_FILE_INFO</a> structure that receives the original INF file name and catalog file information returned by 
<b>SetupQueryInfOriginalFileInformation</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

