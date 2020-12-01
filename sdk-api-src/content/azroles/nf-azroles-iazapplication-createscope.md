---
UID: NF:azroles.IAzApplication.CreateScope
title: IAzApplication::CreateScope (azroles.h)
description: Creates an IAzScope object with the specified name.
helpviewer_keywords: ["AzApplication object [Security]","CreateScope method","CreateScope","CreateScope method [Security]","CreateScope method [Security]","AzApplication object","CreateScope method [Security]","IAzApplication interface","IAzApplication interface [Security]","CreateScope method","IAzApplication.CreateScope","IAzApplication::CreateScope","azroles/IAzApplication::CreateScope","security.iazapplication_createscope"]
old-location: security\iazapplication_createscope.htm
tech.root: security
ms.assetid: 6d5044d8-0b6a-4681-a8eb-e93f50fbdf36
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],CreateScope method, CreateScope, CreateScope method [Security], CreateScope method [Security],AzApplication object, CreateScope method [Security],IAzApplication interface, IAzApplication interface [Security],CreateScope method, IAzApplication.CreateScope, IAzApplication::CreateScope, azroles/IAzApplication::CreateScope, security.iazapplication_createscope
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication::CreateScope
 - azroles/IAzApplication::CreateScope
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.CreateScope
 - AzApplication.CreateScope
---

# IAzApplication::CreateScope


## -description

The <b>CreateScope</b> method creates an <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object with the specified name.

## -parameters

### -param bstrScopeName [in]

Name for the new <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppScope [out]

A pointer to a pointer to the created <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-submit">IAzScope::Submit</a> method to persist any changes made to the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.