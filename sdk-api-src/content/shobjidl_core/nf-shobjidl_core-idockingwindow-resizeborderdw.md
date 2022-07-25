---
UID: NF:shobjidl_core.IDockingWindow.ResizeBorderDW
title: IDockingWindow::ResizeBorderDW (shobjidl_core.h)
description: Notifies the docking window object that the frame's border space has changed. In response to this method, the IDockingWindow implementation must call SetBorderSpaceDW, even if no border space is required or a change is not necessary.
helpviewer_keywords: ["IDockingWindow interface [Windows Shell]","ResizeBorderDW method","IDockingWindow.ResizeBorderDW","IDockingWindow::ResizeBorderDW","ResizeBorderDW","ResizeBorderDW method [Windows Shell]","ResizeBorderDW method [Windows Shell]","IDockingWindow interface","_win32_IDockingWindow_ResizeBorderDW","shell.IDockingWindow_ResizeBorderDW","shobjidl_core/IDockingWindow::ResizeBorderDW"]
old-location: shell\IDockingWindow_ResizeBorderDW.htm
tech.root: shell
ms.assetid: de61badd-0794-484c-921f-4e72e881579c
ms.date: 12/05/2018
ms.keywords: IDockingWindow interface [Windows Shell],ResizeBorderDW method, IDockingWindow.ResizeBorderDW, IDockingWindow::ResizeBorderDW, ResizeBorderDW, ResizeBorderDW method [Windows Shell], ResizeBorderDW method [Windows Shell],IDockingWindow interface, _win32_IDockingWindow_ResizeBorderDW, shell.IDockingWindow_ResizeBorderDW, shobjidl_core/IDockingWindow::ResizeBorderDW
req.header: shobjidl_core.h
req.include-header: Shlobj.h
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
 - IDockingWindow::ResizeBorderDW
 - shobjidl_core/IDockingWindow::ResizeBorderDW
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
 - IDockingWindow.ResizeBorderDW
---

# IDockingWindow::ResizeBorderDW


## -description

Notifies the docking window object that the frame's border space has changed. In response to this method, the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> implementation must call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-setborderspacedw">SetBorderSpaceDW</a>, even if no border space is required or a change is not necessary.

## -parameters

### -param prcBorder

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the frame's available border space.

### -param punkToolbarSite

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the site's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. The docking window object should call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method for this interface, requesting IID_IDockingWindowSite. The docking window object then uses that interface to negotiate its border space. It is the docking window object's responsibility to release this interface when it is no longer needed.

### -param fReserved

Type: <b>BOOL</b>

Reserved. This parameter should always be zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>prcBorder</i> parameter contains the frame's entire available border space. The docking window object should negotiate its border space and then use this information to position itself.

For example, if the docking window object requires 25 pixels at the top of the border space, it should negotiate for this through the following steps:

                

<ol>
<li>Allocate a <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure and set its <b>top</b> member to 25.</li>
<li>Call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-requestborderspacedw">RequestBorderSpaceDW</a> to request the space.</li>
<li>If the request is approved by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-requestborderspacedw">RequestBorderSpaceDW</a>, call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idockingwindowsite-setborderspacedw">SetBorderSpaceDW</a> to allocate the space.</li>
</ol>
 
                
                The docking window object can then position its window at prcBorder-&gt;left and prcBorder-&gt;top. The width of the docking window object's window is determined by subtracting prcBorder-&gt;left from prcBorder-&gt;right. Its height is contained in the <b>top</b> member of the <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>



<a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe">IDockingWindowFrame</a>



<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite">IDockingWindowSite</a>