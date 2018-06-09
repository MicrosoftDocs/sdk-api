---
UID: NF:tokenbinding.TokenBindingDeleteBinding
title: TokenBindingDeleteBinding function
author: windows-sdk-content
description: Deletes the token binding key that is associated with the specified target string.
old-location: security\tokenbindingdeletebinding.htm
old-project: SecCNG
ms.assetid: 4258CC92-580E-403C-9AE4-4BB726255464
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: TokenBindingDeleteBinding, TokenBindingDeleteBinding function [Security], security.tokenbindingdeletebinding, tokenbinding/TokenBindingDeleteBinding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tokenbinding.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: TOKENBINDING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - tokenbinding.dll
api_name:
 - TokenBindingDeleteBinding
product: Windows
targetos: Windows
req.lib: Tokenbinding.lib
req.dll: Tokenbinding.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TokenBindingDeleteBinding function


## -description


Deletes the token binding key that is associated with the specified target string.


## -parameters




### -param targetURL [in]

The target string for which <b>TokenBindingDeleteBinding</b> should delete the associated token binding key.


## -returns



Returns a status code that indicates the success or failure of the function.




## -remarks



You can call <b>TokenBindingDeleteBinding</b> from user mode. 




## -see-also




<a href="https://msdn.microsoft.com/4289E3F0-17AC-485B-A326-2C8BECD5CABB">TokenBindingGenerateBinding</a>
 

 

