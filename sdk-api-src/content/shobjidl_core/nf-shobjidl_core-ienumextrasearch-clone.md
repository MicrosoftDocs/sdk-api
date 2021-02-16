---
UID: NF:shobjidl_core.IEnumExtraSearch.Clone
title: IEnumExtraSearch::Clone (shobjidl_core.h)
description: Used to request a duplicate of the enumerator object to preserve its current state.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","IEnumExtraSearch interface","IEnumExtraSearch interface [Windows Shell]","Clone method","IEnumExtraSearch.Clone","IEnumExtraSearch::Clone","_win32_IEnumExtraSearch_Clone","shell.IEnumExtraSearch_Clone","shobjidl_core/IEnumExtraSearch::Clone"]
old-location: shell\IEnumExtraSearch_Clone.htm
tech.root: shell
ms.assetid: 9d766cf9-784b-4e89-ad58-bab6415630fe
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumExtraSearch interface, IEnumExtraSearch interface [Windows Shell],Clone method, IEnumExtraSearch.Clone, IEnumExtraSearch::Clone, _win32_IEnumExtraSearch_Clone, shell.IEnumExtraSearch_Clone, shobjidl_core/IEnumExtraSearch::Clone
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumExtraSearch::Clone
 - shobjidl_core/IEnumExtraSearch::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumExtraSearch.Clone
---

# IEnumExtraSearch::Clone


## -description

Used to request a duplicate of the enumerator object to preserve its current state.

## -parameters

### -param ppenum

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch">IEnumExtraSearch</a>**</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch">IEnumExtraSearch</a> interface of a new enumerator object.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.

## -remarks

The new enumerator should be created with the same state as the current one. Use the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumextrasearch-skip">IEnumExtraSearch::Skip</a> method to advance the enumeration index to the appropriate value before returning.