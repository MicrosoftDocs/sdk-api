---
UID: NF:d2d1svg.ID2D1SvgElement.InsertChildBefore
title: ID2D1SvgElement::InsertChildBefore
author: windows-sdk-content
description: Inserts newChild as a child of this element, before the referenceChild element.
old-location: direct2d\id2d1svgelement_insertchildbefore.htm
tech.root: direct2d
ms.assetid: 09BBABC1-0644-473E-A751-C84437941A2B
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1SvgElement interface [Direct2D],InsertChildBefore method, ID2D1SvgElement.InsertChildBefore, ID2D1SvgElement::InsertChildBefore, InsertChildBefore, InsertChildBefore method [Direct2D], InsertChildBefore method [Direct2D],ID2D1SvgElement interface, d2d1svg/ID2D1SvgElement::InsertChildBefore, direct2d.id2d1svgelement_insertchildbefore
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
 - ID2D1SvgElement.InsertChildBefore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::InsertChildBefore


## -description


Inserts newChild as a child of this element, before the referenceChild element.
         If the newChild element already has a parent, it is removed from this parent as
        part of the insertion.
      


## -parameters




### -param newChild [in]

Type: <b>ID2D1SvgElement*</b>

The element to be inserted.


### -param referenceChild [in, optional]

Type: <b>ID2D1SvgElement*</b>

The element that the child should be inserted before.
            If referenceChild is null, the newChild is placed as the last child.
            If referenceChild is non-null, it must be an immediate child of this element.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code. Returns an error if this element cannot accept children
            of the type of newChild. Returns an error if the newChild is an ancestor of this
            element.
          




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

