---
UID: NF:mfidl.CreatePropertyStore
title: CreatePropertyStore function (mfidl.h)
description: Creates an empty property store object.
helpviewer_keywords: ["CreatePropertyStore","CreatePropertyStore function [Media Foundation]","bb0d32ef-ec16-4341-8b66-d57ebec785f9","mf.createpropertystore","mfidl/CreatePropertyStore"]
old-location: mf\createpropertystore.htm
tech.root: mf
ms.assetid: bb0d32ef-ec16-4341-8b66-d57ebec785f9
ms.date: 12/05/2018
ms.keywords: CreatePropertyStore, CreatePropertyStore function [Media Foundation], bb0d32ef-ec16-4341-8b66-d57ebec785f9, mf.createpropertystore, mfidl/CreatePropertyStore
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreatePropertyStore
 - mfidl/CreatePropertyStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - CreatePropertyStore
---

# CreatePropertyStore function


## -description

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Instead, applications should use the <b>PSCreateMemoryPropertyStore</b> function to create property stores.]

Creates an empty property store object.

## -parameters

### -param ppStore [out]

Receives a pointer to the <b>IPropertyStore</b> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>