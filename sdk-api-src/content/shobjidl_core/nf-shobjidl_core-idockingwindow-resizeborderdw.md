---
UID: NF:shobjidl_core.IDockingWindow.ResizeBorderDW
title: IDockingWindow::ResizeBorderDW
author: windows-sdk-content
description: Notifies the docking window object that the frame's border space has changed. In response to this method, the IDockingWindow implementation must call SetBorderSpaceDW, even if no border space is required or a change is not necessary.
old-location: shell\IDockingWindow_ResizeBorderDW.htm
tech.root: shell
ms.assetid: de61badd-0794-484c-921f-4e72e881579c
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IDockingWindow interface [Windows Shell],ResizeBorderDW method, IDockingWindow.ResizeBorderDW, IDockingWindow::ResizeBorderDW, ResizeBorderDW, ResizeBorderDW method [Windows Shell], ResizeBorderDW method [Windows Shell],IDockingWindow interface, _win32_IDockingWindow_ResizeBorderDW, shell.IDockingWindow_ResizeBorderDW, shobjidl_core/IDockingWindow::ResizeBorderDW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDockingWindow.ResizeBorderDW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockingWindow::ResizeBorderDW


## -description


Notifies the docking window object that the frame's border space has changed. In response to this method, the <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> implementation must call <a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">SetBorderSpaceDW</a>, even if no border space is required or a change is not necessary.


## -parameters




### -param prcBorder

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the frame's available border space.


### -param punkToolbarSite

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the site's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. The docking window object should call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method for this interface, requesting IID_IDockingWindowSite. The docking window object then uses that interface to negotiate its border space. It is the docking window object's responsibility to release this interface when it is no longer needed.


### -param fReserved

Type: <b>BOOL</b>

Reserved. This parameter should always be zero.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>prcBorder</i> parameter contains the frame's entire available border space. The docking window object should negotiate its border space and then use this information to position itself.

For example, if the docking window object requires 25 pixels at the top of the border space, it should negotiate for this through the following steps:

                

<ol>
<li>Allocate a <a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a> structure and set its <b>top</b> member to 25.</li>
<li>Call <a href="https://msdn.microsoft.com/a104c58b-44da-47e7-b10b-f0116024bee1">RequestBorderSpaceDW</a> to request the space.</li>
<li>If the request is approved by <a href="https://msdn.microsoft.com/a104c58b-44da-47e7-b10b-f0116024bee1">RequestBorderSpaceDW</a>, call <a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">SetBorderSpaceDW</a> to allocate the space.</li>
</ol>
 
                
                The docking window object can then position its window at prcBorder-&gt;left and prcBorder-&gt;top. The width of the docking window object's window is determined by subtracting prcBorder-&gt;left from prcBorder-&gt;right. Its height is contained in the <b>top</b> member of the <a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>



<a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>



<a href="https://msdn.microsoft.com/d0dc10db-316a-4eaa-83db-3f186ee77071">IDockingWindowFrame</a>



<a href="https://msdn.microsoft.com/7418a6af-74ce-4435-8ed9-af106df0f95b">IDockingWindowSite</a>
 

 

