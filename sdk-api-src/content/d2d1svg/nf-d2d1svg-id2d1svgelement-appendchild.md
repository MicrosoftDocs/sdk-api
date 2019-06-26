---
UID: NF:d2d1svg.ID2D1SvgElement.AppendChild
title: ID2D1SvgElement::AppendChild (d2d1svg.h)
author: windows-sdk-content
description: Appends an element to the list of children.
old-location: direct2d\id2d1svgelement_appendchild.htm
tech.root: Direct2D
ms.assetid: BE9F0820-D66E-4B20-8790-3D5B3652754B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AppendChild, AppendChild method [Direct2D], AppendChild method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],AppendChild method, ID2D1SvgElement.AppendChild, ID2D1SvgElement::AppendChild, d2d1svg/ID2D1SvgElement::AppendChild, direct2d.id2d1svgelement_appendchild
ms.topic: method
f1_keywords: 
 - "d2d1svg/ID2D1SvgElement.AppendChild"
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
 - ID2D1SvgElement.AppendChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgElement::AppendChild


## -description


Appends an element to the list of children. 
        If the element already has a parent, it is removed from this parent as part of the append operation. 
      


## -parameters




### -param newChild [in]

Type: <b>ID2D1SvgElement*</b>

The element to append.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code.
          Returns an error if this element cannot accept children of the type of newChild. 
          Returns an error if the newChild is an ancestor of this element.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>
 

 

