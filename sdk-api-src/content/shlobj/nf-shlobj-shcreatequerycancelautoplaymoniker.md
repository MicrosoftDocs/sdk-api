---
UID: NF:shlobj.SHCreateQueryCancelAutoPlayMoniker
title: SHCreateQueryCancelAutoPlayMoniker function (shlobj.h)
description: Deprecated. Creates a QueryCancelAutoPlay class moniker, which can then be used to register the IQueryCancelAutoPlay handler in the running object table (ROT).
helpviewer_keywords: ["SHCreateQueryCancelAutoPlayMoniker","SHCreateQueryCancelAutoPlayMoniker function [Windows Shell]","_shell_SHCreateQueryCancelAutoPlayMoniker","shell.SHCreateQueryCancelAutoPlayMoniker","shlobj/SHCreateQueryCancelAutoPlayMoniker"]
old-location: shell\SHCreateQueryCancelAutoPlayMoniker.htm
tech.root: shell
ms.assetid: 560a2b30-66f4-4b0f-9d46-ae714491c376
ms.date: 12/05/2018
ms.keywords: SHCreateQueryCancelAutoPlayMoniker, SHCreateQueryCancelAutoPlayMoniker function [Windows Shell], _shell_SHCreateQueryCancelAutoPlayMoniker, shell.SHCreateQueryCancelAutoPlayMoniker, shlobj/SHCreateQueryCancelAutoPlayMoniker
req.header: shlobj.h
req.include-header: 
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateQueryCancelAutoPlayMoniker
 - shlobj/SHCreateQueryCancelAutoPlayMoniker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateQueryCancelAutoPlayMoniker
---

# SHCreateQueryCancelAutoPlayMoniker function


## -description

<p class="CCE_Message">[This function is deprecated. Use <a href="/windows/desktop/api/objbase/nf-objbase-createclassmoniker">CreateClassMoniker</a> instead. Note that the CLSID used in the call to <b>CreateClassMoniker</b> must be application-defined. Do not call <b>CreateClassMoniker</b> with a system-defined CLSID.]

Deprecated. Creates a <b>QueryCancelAutoPlay</b> class moniker, which can then be used to register the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-iquerycancelautoplay">IQueryCancelAutoPlay</a> handler in the running object table (ROT).

## -parameters

### -param ppmoniker [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>**</b>

The address of a <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface pointer that, when this function returns successfully, receives the <b>QueryCancelAutoPlay</b> class moniker. If this function call fails, this value is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If successful, <b>SHCreateQueryCancelAutoPlayMoniker</b> calls the interface's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method and increments the reference count. When you are finished, call the interface's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method to release.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-createclassmoniker">CreateClassMoniker</a>