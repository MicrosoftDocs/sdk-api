---
UID: NE:tokenbinding.TOKENBINDING_TYPE
title: TOKENBINDING_TYPE
author: windows-sdk-content
description: Specifies the possible types for a token binding.
old-location: security\tokenbinding_type.htm
tech.root: seccng
ms.assetid: 7F126B3E-1033-4C0A-AD5F-0FAD951C85C6
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: TOKENBINDING_TYPE, TOKENBINDING_TYPE enumeration [Security], TOKENBINDING_TYPE_PROVIDED, TOKENBINDING_TYPE_REFERRED, security.tokenbinding_type, tokenbinding/TOKENBINDING_TYPE, tokenbinding/TOKENBINDING_TYPE_PROVIDED, tokenbinding/TOKENBINDING_TYPE_REFERRED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tokenbinding.h
api_name:
 - TOKENBINDING_TYPE
product: Windows
targetos: Windows
req.typenames: TOKENBINDING_TYPE
req.redist: 
---

# TOKENBINDING_TYPE enumeration


## -description


Specifies the possible types for a token binding.


## -enum-fields




### -field TOKENBINDING_TYPE_PROVIDED

This type of Token Binding is used to protect tokens issued by the Identity Provider for the client to present with subsequent requests back to this Identity Provider.


### -field TOKENBINDING_TYPE_REFERRED

This type of Token Binding is used to protect tokens issued by the Identity Provider for the client to present to a Relying Party.


## -remarks



More information about the use of these Token Binding types can be found in the <b>Token Binding over HTTP Internet</b> draft.




## -see-also




<a href="https://msdn.microsoft.com/4289E3F0-17AC-485B-A326-2C8BECD5CABB">TokenBindingGenerateBinding</a>
 

 

