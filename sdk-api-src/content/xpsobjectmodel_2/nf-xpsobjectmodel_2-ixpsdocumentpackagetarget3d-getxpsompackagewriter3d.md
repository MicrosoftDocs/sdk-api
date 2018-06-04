---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IXpsDocumentPackageTarget3D::GetXpsOMPackageWriter3D


## -description


Gets a new <a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a> object for the document package.


## -parameters




### -param documentSequencePartName [in]

The root part of XPS payload.


### -param discardControlPartName [in, optional]

The discard control part for the XPS payload. 


### -param modelPartName [in]

Name of the part which will hold the 3D model. The part’s content type is “application/vnd.ms-package.3dmanufacturing-3dmodel+xml”. It is linked from package root with relationship type “http://schemas.microsoft.com/3dmanufacturing/2013/01/3dmodel” .


### -param modelData [in]

A readable stream which holds 3D model description. The model description may be UTF16 encoding of XML document, but for XPS OM and XpsPrint, this is a BLOB passing through. The <b>GetXpsOMPackageWriter3D</b> method attempts to move the provided stream’s read pointer to the beginning of the stream, but the method call will not fail if the stream does not support the <a href="http://go.microsoft.com/fwlink/p/?LinkID=301232">Seek</a> method.


### -param packageWriter






#### - ppWriter3D [out]

 Returns the writer which may be used to send XPS content and textures for the 3D model.



## -returns



Returns the appropriate HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/7273235D-EB74-4FB2-B471-FCFF71741BF6">IXpsDocumentPackageTarget3D</a>
 

 

