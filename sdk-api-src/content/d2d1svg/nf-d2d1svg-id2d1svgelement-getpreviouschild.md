---
UID: NF:d2d1svg.ID2D1SvgElement.GetPreviousChild
title: ID2D1SvgElement::GetPreviousChild
author: windows-sdk-content
description: Gets the previous sibling of the referenceChild element.
old-location: direct2d\id2d1svgelement_getpreviouschild.htm
tech.root: Direct2D
ms.assetid: CE4334D8-7A96-464A-BE57-A7B226221FC3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetPreviousChild, GetPreviousChild method [Direct2D], GetPreviousChild method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetPreviousChild method, ID2D1SvgElement.GetPreviousChild, ID2D1SvgElement::GetPreviousChild, d2d1svg/ID2D1SvgElement::GetPreviousChild, direct2d.id2d1svgelement_getpreviouschild
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
 - ID2D1SvgElement.GetPreviousChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::GetPreviousChild


## -description


Gets the previous sibling of the referenceChild element.


## -parameters




### -param referenceChild [in]

Type: <b>ID2D1SvgElement*</b>

The referenceChild must be an immediate child of this element.


### -param previousChild

Type: <b>ID2D1SvgElement**</b>

The output previousChild element will be non-null if the referenceChild has a previous sibling. If the referenceChild is the first child, the output is null.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

