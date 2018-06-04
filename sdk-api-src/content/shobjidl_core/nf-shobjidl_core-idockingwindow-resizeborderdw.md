---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDockingWindow::ResizeBorderDW


## -description


Notifies the docking window object that the frame's border space has changed. In response to this method, the <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> implementation must call <a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">SetBorderSpaceDW</a>, even if no border space is required or a change is not necessary.


## -parameters




### -param prcBorder

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the frame's available border space.


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
 

 

