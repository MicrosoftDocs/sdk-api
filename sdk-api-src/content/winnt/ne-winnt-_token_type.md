---
UID: NE:winnt._TOKEN_TYPE
title: "_TOKEN_TYPE"
author: windows-sdk-content
description: Contains values that differentiate between a primary token and an impersonation token.
old-location: security\token_type.htm
tech.root: secauthz
ms.assetid: 51b6717e-3fda-4af4-8995-4ac571eae2fd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTOKEN_TYPE, PTOKEN_TYPE, PTOKEN_TYPE enumeration pointer [Security], TOKEN_TYPE, TOKEN_TYPE enumeration [Security], TokenImpersonation, TokenPrimary, _TOKEN_TYPE, _win32_token_type_str, security.token_type, winnt/PTOKEN_TYPE, winnt/TOKEN_TYPE, winnt/TokenImpersonation, winnt/TokenPrimary"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - TOKEN_TYPE
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
req.redist: 
---

# _TOKEN_TYPE enumeration


## -description


The <b>TOKEN_TYPE</b> enumeration contains values that differentiate between a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> and an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>.
		


## -enum-fields




### -field TokenPrimary

Indicates a primary token.


### -field TokenImpersonation

Indicates an impersonation token.


## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/b87c942b-8e58-471d-8cdf-e46cdac647c4">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/29fb738f-1ecd-4b72-9aea-64698cd74c12">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/cb606665-1266-4e71-a145-9b04bf157cdc">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/85617d56-ad46-40a3-a335-121f3c8edcc3">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/d23ebe6c-36a3-434a-a0fa-fcdf50dd19a0">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/c9016511-740f-44f3-92ed-17cc518c6612">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/9c533327-e4a0-4852-828c-622d190b7d1e">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/7fcc4a46-1bac-49c1-a239-b466d3bf31d9">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/5dd8172d-7b1a-4cc0-b667-5fe91d278393">TOKEN_USER</a>
 

 

