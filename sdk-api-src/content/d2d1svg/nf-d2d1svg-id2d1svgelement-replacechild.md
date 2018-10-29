---
UID: NF:d2d1svg.ID2D1SvgElement.ReplaceChild
title: ID2D1SvgElement::ReplaceChild
author: windows-sdk-content
description: Replaces the oldChild element with the newChild.
old-location: direct2d\id2d1svgelement_replacechild.htm
tech.root: Direct2D
ms.assetid: BEF74F58-D218-46CA-AE02-F15DDAC48FB4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],ReplaceChild method, ID2D1SvgElement.ReplaceChild, ID2D1SvgElement::ReplaceChild, ReplaceChild, ReplaceChild method [Direct2D], ReplaceChild method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::ReplaceChild, direct2d.id2d1svgelement_replacechild
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID2D1SvgElement.ReplaceChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::ReplaceChild


## -description


Replaces the oldChild element with the newChild. This operation removes the oldChild from the tree.
        If the newChild element already has a parent, it is removed from this parent as part of the replace operation.
      


## -parameters




### -param newChild [in]

Type: <b>ID2D1SvgElement*</b>

The element to be inserted.


### -param oldChild [in]

Type: <b>ID2D1SvgElement*</b>

The child element to be replaced. The oldChild element must be an immediate child of this element.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if
            this element cannot accept children of the type of newChild. Returns an error if
            the newChild is an ancestor of this element.
          




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

