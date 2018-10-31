---
UID: NF:d2d1svg.ID2D1SvgDocument.Serialize
title: ID2D1SvgDocument::Serialize
author: windows-sdk-content
description: Serializes an element and its subtree to XML. The output XML is encoded as UTF-8.
old-location: direct2d\id2d1svgdocument_serialize.htm
tech.root: direct2d
ms.assetid: 799E975A-F3BF-4832-AE51-DA064E5C698E
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ID2D1SvgDocument interface [Direct2D],Serialize method, ID2D1SvgDocument.Serialize, ID2D1SvgDocument::Serialize, Serialize, Serialize method [Direct2D], Serialize method [Direct2D],ID2D1SvgDocument interface, d2d1svg/ID2D1SvgDocument::Serialize, direct2d.id2d1svgdocument_serialize
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
 - ID2D1SvgDocument.Serialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgDocument::Serialize


## -description


Serializes an element and its subtree to XML. The output XML is encoded as UTF-8.


## -parameters




### -param outputXmlStream [in]

Type: <b>IStream*</b>

An output stream to contain the SVG XML subtree.


### -param subtree [in, optional]

Type: <b>ID2D1SvgElement*</b>

The root of the subtree. If null, the entire document is serialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/1F570A77-7110-4C71-A7BE-74F2B78CFE96">ID2D1SvgDocument</a>
 

 

