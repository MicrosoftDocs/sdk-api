---
UID: NF:strmif.IOverlay.GetClipList
title: IOverlay::GetClipList (strmif.h)
description: The GetClipList method retrieves the clipping list.
helpviewer_keywords: ["GetClipList","GetClipList method [DirectShow]","GetClipList method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","GetClipList method","IOverlay.GetClipList","IOverlay::GetClipList","IOverlayGetClipList","dshow.ioverlay_getcliplist","strmif/IOverlay::GetClipList"]
old-location: dshow\ioverlay_getcliplist.htm
tech.root: dshow
ms.assetid: 3133bcae-0a08-45e9-b70a-07ea6ffef8ee
ms.date: 12/05/2018
ms.keywords: GetClipList, GetClipList method [DirectShow], GetClipList method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetClipList method, IOverlay.GetClipList, IOverlay::GetClipList, IOverlayGetClipList, dshow.ioverlay_getcliplist, strmif/IOverlay::GetClipList
f1_keywords:
- strmif/IOverlay.GetClipList
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IOverlay.GetClipList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlay::GetClipList


## -description



The <code>GetClipList</code> method retrieves the clipping list.




## -parameters




### -param pSourceRect [out]

Pointer to the bounding client rectangle.


### -param pDestinationRect [in]

Pointer to the destination rectangle.


### -param ppRgnData [out]

Address of a pointer to the header and data describing clipping. If successful, free the allocated memory by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay</a> implementation allocates the memory for the clipping rectangles, because it can vary in length. The filter calling this method should free the memory (using <b>CoTaskMemFree</b>) when it is finished with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>
 

 

