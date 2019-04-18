---
UID: NF:d2d1svg.ID2D1SvgElement.CreateChild
title: ID2D1SvgElement::CreateChild (d2d1svg.h)
author: windows-sdk-content
description: Creates an element from a tag name. The element is appended to the list of children.
old-location: direct2d\id2d1svgelement_createchild.htm
tech.root: Direct2D
ms.assetid: E8BD0808-D3A3-41BB-A7A3-2183C0E56396
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateChild, CreateChild method [Direct2D], CreateChild method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],CreateChild method, ID2D1SvgElement.CreateChild, ID2D1SvgElement::CreateChild, d2d1svg/ID2D1SvgElement::CreateChild, direct2d.id2d1svgelement_createchild
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
 - ID2D1SvgElement.CreateChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgElement::CreateChild


## -description


Creates an element from a tag name. The element is appended to the list of children. 


## -parameters




### -param tagName [in]

Type: <b>PCWSTR</b>

The tag name of the new child. An empty string is interpreted to be a text content element.


### -param newChild [out]

Type: <b>ID2D1SvgElement**</b>

The new child element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.
          Returns an error if this element cannot accept children of the specified type.
          




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

