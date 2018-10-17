---
UID: NF:d2d1svg.ID2D1SvgElement.GetNextChild
title: ID2D1SvgElement::GetNextChild
author: windows-sdk-content
description: Gets the next sibling of the referenceChild element.
old-location: direct2d\id2d1svgelement_getnextchild.htm
tech.root: direct2d
ms.assetid: 41D48F64-3C90-4CB1-91F5-32FC04042471
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetNextChild, GetNextChild method [Direct2D], GetNextChild method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetNextChild method, ID2D1SvgElement.GetNextChild, ID2D1SvgElement::GetNextChild, d2d1svg/ID2D1SvgElement::GetNextChild, direct2d.id2d1svgelement_getnextchild
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
 - ID2D1SvgElement.GetNextChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::GetNextChild


## -description


Gets the next sibling of the referenceChild element.


## -parameters




### -param referenceChild [in]

Type: <b>ID2D1SvgElement*</b>

The referenceChild must be an immediate child of this element.


### -param nextChild

Type: <b>ID2D1SvgElement**</b>

The output nextChild element will be non-null if the referenceChild has a next sibling. If the referenceChild is the last child, the output is null.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

