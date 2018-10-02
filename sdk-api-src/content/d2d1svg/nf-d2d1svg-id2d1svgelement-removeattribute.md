---
UID: NF:d2d1svg.ID2D1SvgElement.RemoveAttribute
title: ID2D1SvgElement::RemoveAttribute
author: windows-sdk-content
description: Removes the attribute from this element.
old-location: direct2d\id2d1svgelement_removeattribute.htm
tech.root: direct2d
ms.assetid: 608BB970-CC78-4CF3-BD8C-02DCBBFA287E
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],RemoveAttribute method, ID2D1SvgElement.RemoveAttribute, ID2D1SvgElement::RemoveAttribute, RemoveAttribute, RemoveAttribute method [Direct2D], RemoveAttribute method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::RemoveAttribute, direct2d.id2d1svgelement_removeattribute
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
 - ID2D1SvgElement.RemoveAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::RemoveAttribute


## -description


Removes the attribute from this element.  Also removes this attribute from within
        an inline style if present.
      


## -parameters




### -param name [in]

Type: <b>PCWSTR</b>

The name of the attribute to remove.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if the attribute name is not valid
            on this element.
          




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

