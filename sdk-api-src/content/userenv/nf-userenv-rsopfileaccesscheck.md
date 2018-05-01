---
UID: NF:userenv.RsopFileAccessCheck
title: RsopFileAccessCheck function
author: windows-driver-content
description: The RSoPFileAccessCheck function determines whether a file's security descriptor grants a specified set of file access rights to the client identified by an RSOPTOKEN.
old-location: policy\rsopfileaccesscheck.htm
old-project: Policy
ms.assetid: dfdf14ee-fee1-4e96-9955-7f24dfe39487
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: RSoPFileAccessCheck, RSoPFileAccessCheck function [Group Policy], RsopFileAccessCheck, _win32_rsopfileaccesscheck, policy.rsopfileaccesscheck, userenv/RSoPFileAccessCheck
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	RSoPFileAccessCheck
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# RsopFileAccessCheck function


## -description


The
    <b>RSoPFileAccessCheck</b> function determines whether a file's security descriptor grants a specified set of file access rights to the client identified by an <b>RSOPTOKEN</b>.


## -parameters




### -param pszFileName [in]

Pointer to the name of the relevant file. The file must already exist.


### -param pRsopToken [in]

Pointer to a valid <b>RSOPTOKEN</b> representing the client attempting to gain access to the file.


### -param dwDesiredAccessMask [in]

Specifies an access mask that indicates the access rights to check. This mask can contain a combination of 
<a href="https://msdn.microsoft.com/e18cede9-9bf7-4866-850b-5d7fa43a5b0f">generic</a>, 
<a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">standard</a>, and specific access rights. For more information, see 
<a href="https://msdn.microsoft.com/da67c486-d2e7-4632-ac7a-c18aabc3f21d">Access Rights and Access Masks</a>.


### -param pdwGrantedAccessMask [out]

Pointer to an access mask that receives the granted access rights.

If the function succeeds, the <i>pbAccessStatus</i> parameter is set to <b>TRUE</b>, and the mask is updated to contain the standard and specific rights granted. If <i>pbAccessStatus</i> is set to <b>FALSE</b>, this parameter is set to zero. If the function fails, the mask is not modified.


### -param pbAccessStatus [out]

Pointer to a variable that receives the results of the access check.

If the function succeeds, and the requested set of access rights are granted, this parameter is set to <b>TRUE</b>. Otherwise, this parameter is set to <b>FALSE</b>. If the function fails, the status is not modified.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



The 
<b>RSoPFileAccessCheck</b> function indicates, in the <i>pbAccessStatus</i> parameter, whether access is granted or denied to the client identified by the <b>RSOPTOKEN</b>. If access is granted, the requested access mask becomes the object's granted access mask.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/d63734a0-1a88-4669-828e-de467606fc14">RSoPAccessCheckByType</a>
 

 

