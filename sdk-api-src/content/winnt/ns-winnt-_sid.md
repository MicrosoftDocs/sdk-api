---
UID: NS:winnt._SID
title: "_SID"
author: windows-sdk-content
description: Used to uniquely identify users or groups.
old-location: security\sid.htm
tech.root: secauthz
ms.assetid: 328fba4e-e590-4174-9274-52dad58cb91f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PISID, PSID, PSID structure pointer [Security], SID, SID structure [Security], _SID, _win32_sid_str, security.sid, winnt/PSID, winnt/SID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SID
product: Windows
targetos: Windows
req.typenames: SID, *PISID
req.redist: 
---

# _SID structure


## -description


The security identifier (SID) structure is a variable-length structure used to uniquely identify users or groups.
			

Applications should not modify a SID directly. To create and manipulate a security identifier, use the functions listed in the See Also section.


## -struct-fields


## -see-also




<a href="https://msdn.microsoft.com/fcdff2f8-7f43-4c0f-b548-4914b1991937">AllocateAndInitializeSid</a>



<a href="https://msdn.microsoft.com/e673e727-edb1-450c-9e1a-a3dc90acc929">ConvertSidToStringSid</a>



<a href="https://msdn.microsoft.com/bf7262e3-ad2c-44c4-99cb-dcf29ad36efd">ConvertStringSidToSid</a>



<a href="https://msdn.microsoft.com/2d7c182e-cdf8-4604-97bf-468bb4bd9232">CopySid</a>



<a href="https://msdn.microsoft.com/08420df3-f6e6-462e-a2e6-d2a7a90be8ed">EqualSid</a>



<a href="https://msdn.microsoft.com/1e2098d8-4d1f-4353-97c1-549021a5b3fd">FreeSid</a>



<a href="https://msdn.microsoft.com/0acaa804-494c-4d69-b1f7-8d167b494761">GetLengthSid</a>



<a href="https://msdn.microsoft.com/67a06e7b-775f-424c-ab36-0fc9b93b801a">GetSidIdentifierAuthority</a>



<a href="https://msdn.microsoft.com/a481fb4f-20bd-4f44-a3d5-d8b8d6228339">GetSidLengthRequired</a>



<a href="https://msdn.microsoft.com/3a2d07f3-f1da-477d-b93f-525e3459dc61">GetSidSubAuthority</a>



<a href="https://msdn.microsoft.com/ca81fb91-f5a1-4dc6-83ec-eadb62a37805">GetSidSubAuthorityCount</a>



<a href="https://msdn.microsoft.com/b2d803a5-faaf-4066-ba2c-0442c71bb150">InitializeSid</a>



<a href="https://msdn.microsoft.com/0fb08512-90a1-4a5c-9b4c-121bf7701bba">IsValidSid</a>



<a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a>



<a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a>



<a href="https://msdn.microsoft.com/528412e7-c2b6-4ddd-86de-999252972421">SID Components</a>
 

 

