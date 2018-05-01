---
UID: NS:winnt._TOKEN_DEFAULT_DACL
title: "_TOKEN_DEFAULT_DACL"
author: windows-driver-content
description: Specifies a discretionary access control list (DACL).
old-location: security\token_default_dacl.htm
old-project: SecAuthZ
ms.assetid: 29fb738f-1ecd-4b72-9aea-64698cd74c12
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PTOKEN_DEFAULT_DACL, PTOKEN_DEFAULT_DACL, PTOKEN_DEFAULT_DACL structure pointer [Security], TOKEN_DEFAULT_DACL, TOKEN_DEFAULT_DACL structure [Security], _TOKEN_DEFAULT_DACL, _win32_token_default_dacl_str, security.token_default_dacl, winnt/PTOKEN_DEFAULT_DACL, winnt/TOKEN_DEFAULT_DACL"
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
req.typenames: TOKEN_DEFAULT_DACL, *PTOKEN_DEFAULT_DACL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	TOKEN_DEFAULT_DACL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _TOKEN_DEFAULT_DACL structure


## -description


The <b>TOKEN_DEFAULT_DACL</b> structure specifies a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL).


## -struct-fields




### -field DefaultDacl

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> structure assigned by default to any objects created by the user. The user is represented by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>.
						


## -remarks



The <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function retrieves the default DACL for an access token, in the form of a <b>TOKEN_DEFAULT_DACL</b> structure. This structure is also used with the <a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a> function to set the default DACL.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556827">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556838">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556842">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556845">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556849">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556851">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a>
 

 

