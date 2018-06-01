---
UID: NF:aclapi.FreeInheritedFromArray
title: FreeInheritedFromArray function
author: windows-sdk-content
description: Frees memory allocated by the GetInheritanceSource function.
old-location: security\freeinheritedfromarray.htm
old-project: SecAuthZ
ms.assetid: c9c58b9a-1b65-40e2-b518-30e247f9718e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: FreeInheritedFromArray, FreeInheritedFromArray function [Security], _win32_freeinheritedfromarray, aclapi/FreeInheritedFromArray, security.freeinheritedfromarray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
-	APIRef
-	kbSyntax
 - apiref
: 
api_type:
-	DllExport
 - HeaderDef
: 
api_location:
-	Advapi32.dll
 - accctrl.h
: 
api_name:
-	FreeInheritedFromArray
 - _ACCESS_MODE
: 
product: Windows
targetos: Windows
 - _MULTIPLE_TRUSTEE_OPERATION
: 
 - _PROGRESS_INVOKE_SETTING
: 
 - _SE_OBJECT_TYPE
: 
 - _TRUSTEE_FORM
: 
 - _TRUSTEE_TYPE
: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
 - _ACTRL_ACCESS_ENTRYA
: 
 - _ACTRL_ACCESS_ENTRYW
: 
 - _ACTRL_ACCESS_ENTRY_LISTA
: 
 - _ACTRL_ACCESS_ENTRY_LISTW
: 
 - _ACTRL_ALISTA
: 
 - _ACTRL_ALISTW
: 
 - _ACTRL_PROPERTY_ENTRYA
: 
 - _ACTRL_PROPERTY_ENTRYW
: 
 - _EXPLICIT_ACCESS_A
: 
 - _EXPLICIT_ACCESS_W
: 
 - _INHERITED_FROMA
: 
 - _INHERITED_FROMW
: 
 - _OBJECTS_AND_NAME_A
: 
 - _OBJECTS_AND_NAME_W
: 
 - _OBJECTS_AND_SID
: 
 - _TRUSTEE_A
: 
 - _TRUSTEE_W
: 
req.irql: 
 - 
: 
 - BuildExplicitAccessWithNameA
: 
 - BuildExplicitAccessWithNameW
: 
 - BuildSecurityDescriptorA
: 
 - BuildSecurityDescriptorW
: 
 - BuildTrusteeWithNameA
: 
 - BuildTrusteeWithNameW
: 
 - BuildTrusteeWithObjectsAndNameA
: 
 - BuildTrusteeWithObjectsAndNameW
: 
 - BuildTrusteeWithObjectsAndSidA
: 
 - BuildTrusteeWithObjectsAndSidW
: 
 - BuildTrusteeWithSidA
: 
 - BuildTrusteeWithSidW
: 
 - FreeInheritedFromArray
: 
---

# FreeInheritedFromArray function


## -description



			The <b>FreeInheritedFromArray</b> function frees memory allocated by the 
<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a> function.


## -parameters




### -param pInheritArray [in]

A pointer to the array of <a href="https://msdn.microsoft.com/6839f67a-6c72-406d-b55e-bc366aaad107">INHERITED_FROM</a> structures returned by <a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>.


### -param AceCnt [in]

Number of entries in <i>pInheritArray</i>.


### -param OPTIONAL

TBD




#### - pfnArray [in, optional]

Unused. Set to <b>NULL</b>.


## -returns




						If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>
 

 

