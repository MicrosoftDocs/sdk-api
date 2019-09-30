---
UID: NF:d2d1svg.ID2D1SvgDocument.SetRoot
title: ID2D1SvgDocument::SetRoot (d2d1svg.h)
author: windows-sdk-content
description: Sets the root element of the document.
old-location: direct2d\id2d1svgdocument_setroot.htm
tech.root: Direct2D
ms.assetid: 076DC8F7-E358-484D-A567-60E80F9D2FC3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SvgDocument interface [Direct2D],SetRoot method, ID2D1SvgDocument.SetRoot, ID2D1SvgDocument::SetRoot, SetRoot, SetRoot method [Direct2D], SetRoot method [Direct2D],ID2D1SvgDocument interface, d2d1svg/ID2D1SvgDocument::SetRoot, direct2d.id2d1svgdocument_setroot
ms.topic: method
f1_keywords: 
 - "d2d1svg/ID2D1SvgDocument.SetRoot"
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Direct2d.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgDocument.SetRoot
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgDocument::SetRoot


## -description


Sets the root element of the document.The root element must be an svg element.
        If the element already exists within an svg tree, it is first removed.
      


## -parameters




### -param root [in, optional]

Type: <b>ID2D1SvgElement*</b>

The new root element of the document.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgdocument">ID2D1SvgDocument</a>
 

 

