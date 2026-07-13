---
UID: NF:tokenbinding.TokenBindingDeleteAllBindings
title: TokenBindingDeleteAllBindings function (tokenbinding.h)
description: Deletes all token binding keys that are associated with the calling user or app container.
helpviewer_keywords: ["TokenBindingDeleteAllBindings","TokenBindingDeleteAllBindings function [Security]","security.tokenbindingdeleteallbindings","tokenbinding/TokenBindingDeleteAllBindings"]
old-location: security\tokenbindingdeleteallbindings.htm
tech.root: security
ms.assetid: 0446F62F-96B4-4F4B-9789-0CD12173E601
ms.date: 12/05/2018
ms.keywords: TokenBindingDeleteAllBindings, TokenBindingDeleteAllBindings function [Security], security.tokenbindingdeleteallbindings, tokenbinding/TokenBindingDeleteAllBindings
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
req.lib: Tokenbinding.lib
req.dll: Tokenbinding.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TokenBindingDeleteAllBindings
 - tokenbinding/TokenBindingDeleteAllBindings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - tokenbinding.dll
api_name:
 - TokenBindingDeleteAllBindings
---

# TokenBindingDeleteAllBindings function


## -description

Deletes all token binding keys that are associated with the calling user or app container.



## -returns

Returns a status code that indicates the success or failure of the function.

## -remarks

You can call <b>TokenBindingDeleteAllBindings</b> from user mode.

## -see-also

<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindingdeletebinding">TokenBindingDeleteBinding</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggeneratebinding">TokenBindingGenerateBinding</a>
