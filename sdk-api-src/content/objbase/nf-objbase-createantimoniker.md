---
UID: NF:objbase.CreateAntiMoniker
title: CreateAntiMoniker function (objbase.h)
description: Creates and returns a new anti-moniker.
helpviewer_keywords: ["CreateAntiMoniker","CreateAntiMoniker function [COM]","_com_CreateAntiMoniker","com.createantimoniker","objbase/CreateAntiMoniker"]
old-location: com\createantimoniker.htm
tech.root: com
ms.assetid: 1f8fcbd6-8f05-4d32-af8a-d8de1b56dacf
ms.date: 12/05/2018
ms.keywords: CreateAntiMoniker, CreateAntiMoniker function [COM], _com_CreateAntiMoniker, com.createantimoniker, objbase/CreateAntiMoniker
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateAntiMoniker
 - objbase/CreateAntiMoniker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
api_name:
 - CreateAntiMoniker
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# CreateAntiMoniker function


## -description

Creates and returns a new anti-moniker.

## -parameters

### -param ppmk [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the new anti-moniker. When successful, the function has called <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the anti-moniker and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. When an error occurs, the anti-moniker pointer is <b>NULL</b>.

## -returns

This function can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

You would call this function only if you are writing your own moniker class (implementing the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface). If you are writing a new moniker class that has no internal structure, you can use <b>CreateAntiMoniker</b> in your implementation of the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-inverse">IMoniker::Inverse</a> method, and then check for an anti-moniker in your implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-composewith">IMoniker::ComposeWith</a>.

Like the ".." directory, which acts as the inverse to any directory name just preceding it in a path, an anti-moniker acts as the inverse of a simple moniker that precedes it in a composite moniker. An anti-moniker is used as the inverse of simple monikers with no internal structure. For example, the system-provided implementations of file monikers, item monikers, and pointer monikers all use anti-monikers as their inverse; consequently, an anti-moniker composed to the right of one of these monikers composes to nothing.

A moniker client (an object that is using a moniker to bind to another object) typically does not know the class of a given moniker, so the client cannot be sure that an anti-moniker is the inverse. Therefore, to get the inverse of a moniker, you would call <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-inverse">IMoniker::Inverse</a> rather than <b>CreateAntiMoniker</b>.

To remove the last piece of a composite moniker, you would do the following:

<ol>
<li>Call <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-enum">IMoniker::Enum</a> on the composite, specifying <b>FALSE</b> as the first parameter. This creates an enumerator that returns the component monikers in reverse order. </li>
<li>Use the enumerator to retrieve the last piece of the composite.</li>
<li>Call <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-inverse">IMoniker::Inverse</a> on that moniker. The moniker returned by <b>Inverse</b> will remove the last piece of the composite.
</li>
</ol>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
