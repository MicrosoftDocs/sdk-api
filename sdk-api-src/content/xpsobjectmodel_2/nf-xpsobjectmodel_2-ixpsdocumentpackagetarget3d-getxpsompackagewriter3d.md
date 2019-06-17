---
UID: NF:xpsobjectmodel_2.IXpsDocumentPackageTarget3D.GetXpsOMPackageWriter3D
title: IXpsDocumentPackageTarget3D::GetXpsOMPackageWriter3D (xpsobjectmodel_2.h)
author: windows-sdk-content
description: Gets a new IXpsOMPackageWriter3D object for the document package.
old-location: xps\ixpsdocumentpackagetarget3d_getxpsompackagewriter3d.htm
tech.root: printdocs
ms.assetid: 2F3A6997-B325-4406-A731-5C2EAD875125
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetXpsOMPackageWriter3D, GetXpsOMPackageWriter3D method [XPS Documents and Packaging], GetXpsOMPackageWriter3D method [XPS Documents and Packaging],IXpsDocumentPackageTarget3D interface, IXpsDocumentPackageTarget3D interface [XPS Documents and Packaging],GetXpsOMPackageWriter3D method, IXpsDocumentPackageTarget3D.GetXpsOMPackageWriter3D, IXpsDocumentPackageTarget3D::GetXpsOMPackageWriter3D, xps.ixpsdocumentpackagetarget3d_getxpsompackagewriter3d, xpsobjectmodel_2/IXpsDocumentPackageTarget3D::GetXpsOMPackageWriter3D
ms.topic: method
f1_keywords: ["xpsobjectmodel_2/IXpsDocumentPackageTarget3D.GetXpsOMPackageWriter3D"]
req.header: xpsobjectmodel_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsObjectModel_2.h
api_name:
 - IXpsDocumentPackageTarget3D.GetXpsOMPackageWriter3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsDocumentPackageTarget3D::GetXpsOMPackageWriter3D


## -description


Gets a new <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a> object for the document package.


## -parameters




### -param documentSequencePartName [in]

The root part of XPS payload.


### -param discardControlPartName [in, optional]

The discard control part for the XPS payload. 


### -param modelPartName [in]

Name of the part which will hold the 3D model. The part’s content type is “application/vnd.ms-package.3dmanufacturing-3dmodel+xml”. It is linked from package root with relationship type “http://schemas.microsoft.com/3dmanufacturing/2013/01/3dmodel” .


### -param modelData [in]

A readable stream which holds 3D model description. The model description may be UTF16 encoding of XML document, but for XPS OM and XpsPrint, this is a BLOB passing through. The <b>GetXpsOMPackageWriter3D</b> method attempts to move the provided stream’s read pointer to the beginning of the stream, but the method call will not fail if the stream does not support the <a href="http://go.microsoft.com/fwlink/p/?LinkID=301232">Seek</a> method.


### -param packageWriter [out]

 Returns the writer which may be used to send XPS content and textures for the 3D model.



## -returns



Returns the appropriate HRESULT error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsdocumentpackagetarget3d">IXpsDocumentPackageTarget3D</a>
 

 

