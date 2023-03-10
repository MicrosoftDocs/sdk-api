---
UID: NF:shlobj_core.IDockingWindowSite.SetBorderSpaceDW
title: IDockingWindowSite::SetBorderSpaceDW (shlobj_core.h)
description: Allocates and reserves border space for an IDockingWindow object.
helpviewer_keywords: ["IDockingWindowSite interface [Windows Shell]","SetBorderSpaceDW method","IDockingWindowSite.SetBorderSpaceDW","IDockingWindowSite::SetBorderSpaceDW","SetBorderSpaceDW","SetBorderSpaceDW method [Windows Shell]","SetBorderSpaceDW method [Windows Shell]","IDockingWindowSite interface","_win32_IDockingWindowSite_SetBorderSpaceDW","shell.IDockingWindowSite_SetBorderSpaceDW","shlobj_core/IDockingWindowSite::SetBorderSpaceDW"]
old-location: shell\IDockingWindowSite_SetBorderSpaceDW.htm
tech.root: shell
ms.assetid: 8c79c983-8a5d-4b52-848d-c85c4e4f86ec
ms.date: 12/05/2018
ms.keywords: IDockingWindowSite interface [Windows Shell],SetBorderSpaceDW method, IDockingWindowSite.SetBorderSpaceDW, IDockingWindowSite::SetBorderSpaceDW, SetBorderSpaceDW, SetBorderSpaceDW method [Windows Shell], SetBorderSpaceDW method [Windows Shell],IDockingWindowSite interface, _win32_IDockingWindowSite_SetBorderSpaceDW, shell.IDockingWindowSite_SetBorderSpaceDW, shlobj_core/IDockingWindowSite::SetBorderSpaceDW
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDockingWindowSite::SetBorderSpaceDW
 - shlobj_core/IDockingWindowSite::SetBorderSpaceDW
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
 - IDockingWindowSite.SetBorderSpaceDW
---

# IDockingWindowSite::SetBorderSpaceDW


## -description

Allocates and reserves border space for an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object.

## -parameters

### -param punkObj [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object for which the border space is being set.

### -param pbw [in]

Type: <b>LPCBORDERWIDTHS</b>

A pointer to a <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure that contains the coordinates of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object's border space. The border space should be approved through a successful call to the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-requestborderspacedw">IDockingWindowSite::RequestBorderSpaceDW</a> method before <b>SetBorderSpaceDW</b> is called with these coordinates.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>