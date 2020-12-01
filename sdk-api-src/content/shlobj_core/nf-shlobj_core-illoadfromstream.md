---
UID: NF:shlobj_core.ILLoadFromStream
title: ILLoadFromStream function (shlobj_core.h)
description: Deprecated. Loads an ITEMIDLIST structure from a stream.
helpviewer_keywords: ["ILLoadFromStream","ILLoadFromStream function [Windows Shell]","_win32_ILLoadFromStream","shell.ILLoadFromStream","shlobj_core/ILLoadFromStream"]
old-location: shell\ILLoadFromStream.htm
tech.root: shell
ms.assetid: 060cc008-eb6a-4359-b84b-05c26d69f793
ms.date: 12/05/2018
ms.keywords: ILLoadFromStream, ILLoadFromStream function [Windows Shell], _win32_ILLoadFromStream, shell.ILLoadFromStream, shlobj_core/ILLoadFromStream
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILLoadFromStream
 - shlobj_core/ILLoadFromStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Windows.Storage.dll
api_name:
 - ILLoadFromStream
---

# ILLoadFromStream function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Deprecated. Loads an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure from a stream.

## -parameters

### -param pstm [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer that indicates the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface that the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> loads from.

### -param pidl [out]

Type: <b>PIDLIST_RELATIVE*</b>

Address of a pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure. <b>ILLoadFromStream</b> allocates the necessary memory for the structure, and assigns the address to this parameter.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error-code otherwise.

## -remarks

When you are finished with the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure, you must free it by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream">ILSaveToStream</a>