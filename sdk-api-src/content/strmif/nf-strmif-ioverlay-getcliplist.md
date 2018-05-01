---
UID: NF:strmif.IOverlay.GetClipList
title: IOverlay::GetClipList method
author: windows-driver-content
description: The GetClipList method retrieves the clipping list.
old-location: dshow\ioverlay_getcliplist.htm
old-project: DirectShow
ms.assetid: 3133bcae-0a08-45e9-b70a-07ea6ffef8ee
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetClipList method [DirectShow], GetClipList method [DirectShow], IOverlay interface, GetClipList,IOverlay.GetClipList, IOverlay, IOverlay interface [DirectShow], GetClipList method, IOverlay::GetClipList, IOverlayGetClipList, dshow.ioverlay_getcliplist, strmif/IOverlay::GetClipList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IOverlay.GetClipList
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IOverlay::GetClipList method


## -description



The <code>GetClipList</code> method retrieves the clipping list.




## -parameters




### -param pSourceRect [out]

Pointer to the bounding client rectangle.


### -param pDestinationRect [in]

Pointer to the destination rectangle.


### -param ppRgnData [out]

Address of a pointer to the header and data describing clipping. If successful, free the allocated memory by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay</a> implementation allocates the memory for the clipping rectangles, because it can vary in length. The filter calling this method should free the memory (using <b>CoTaskMemFree</b>) when it is finished with it.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 

