---
UID: NF:shlobj_core.IDockingWindowSite.RequestBorderSpaceDW
title: IDockingWindowSite::RequestBorderSpaceDW (shlobj_core.h)
description: Approves, modifies, or refuses a request for an IDockingWindow object's border space. The border space is not allocated until the SetBorderSpaceDW method is called.
helpviewer_keywords: ["IDockingWindowSite interface [Windows Shell]","RequestBorderSpaceDW method","IDockingWindowSite.RequestBorderSpaceDW","IDockingWindowSite::RequestBorderSpaceDW","RequestBorderSpaceDW","RequestBorderSpaceDW method [Windows Shell]","RequestBorderSpaceDW method [Windows Shell]","IDockingWindowSite interface","_win32_IDockingWindowSite_RequestBorderSpaceDW","shell.IDockingWindowSite_RequestBorderSpaceDW","shlobj_core/IDockingWindowSite::RequestBorderSpaceDW"]
old-location: shell\IDockingWindowSite_RequestBorderSpaceDW.htm
tech.root: shell
ms.assetid: a104c58b-44da-47e7-b10b-f0116024bee1
ms.date: 12/05/2018
ms.keywords: IDockingWindowSite interface [Windows Shell],RequestBorderSpaceDW method, IDockingWindowSite.RequestBorderSpaceDW, IDockingWindowSite::RequestBorderSpaceDW, RequestBorderSpaceDW, RequestBorderSpaceDW method [Windows Shell], RequestBorderSpaceDW method [Windows Shell],IDockingWindowSite interface, _win32_IDockingWindowSite_RequestBorderSpaceDW, shell.IDockingWindowSite_RequestBorderSpaceDW, shlobj_core/IDockingWindowSite::RequestBorderSpaceDW
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
 - IDockingWindowSite::RequestBorderSpaceDW
 - shlobj_core/IDockingWindowSite::RequestBorderSpaceDW
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
 - IDockingWindowSite.RequestBorderSpaceDW
---

# IDockingWindowSite::RequestBorderSpaceDW


## -description

Approves, modifies, or refuses a request for an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object's border space. The border space is not allocated until the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-setborderspacedw">SetBorderSpaceDW</a> method is called.

## -parameters

### -param punkObj [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> object for which the border space is being requested.

### -param pbw [in]

Type: <b>LPCBORDERWIDTHS</b>

A pointer to a <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure. Before calling this method, the structure must be filled with the desired border space. After the method returns successfully, the structure contains the approved border space. The <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a> object may change these values. If border space is critical, it is the caller's responsibility to determine if the returned border space is sufficient.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the border space request is approved or modified, or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>