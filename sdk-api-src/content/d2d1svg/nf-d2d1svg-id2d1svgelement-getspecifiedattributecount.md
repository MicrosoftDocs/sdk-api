---
UID: NF:d2d1svg.ID2D1SvgElement.GetSpecifiedAttributeCount
title: ID2D1SvgElement::GetSpecifiedAttributeCount
author: windows-sdk-content
description: Returns the number of specified attributes on this element.
old-location: direct2d\id2d1svgelement_getspecifiedattributecount.htm
tech.root: direct2d
ms.assetid: DB683CA6-57B5-4B13-9EB3-269DDCA94667
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetSpecifiedAttributeCount, GetSpecifiedAttributeCount method [Direct2D], GetSpecifiedAttributeCount method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetSpecifiedAttributeCount method, ID2D1SvgElement.GetSpecifiedAttributeCount, ID2D1SvgElement::GetSpecifiedAttributeCount, d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeCount, direct2d.id2d1svgelement_getspecifiedattributecount
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
 - ID2D1SvgElement.GetSpecifiedAttributeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgElement::GetSpecifiedAttributeCount


## -description


Returns the number of specified attributes on this element. Attributes are only considered specified if they are explicitly set on the element or present within an inline style. 
        Properties that receive their value through CSS inheritance are not considered specified. 
        An attribute can become specified if it is set through a method call. 
        It can become unspecified if it is removed via <a href="https://msdn.microsoft.com/608BB970-CC78-4CF3-BD8C-02DCBBFA287E">RemoveAttribute</a>.


## -parameters






## -returns



Type: <b>UINT32</b>

Returns the number of specified attributes on this element. 




## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

