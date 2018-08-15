---
UID: NF:xpsobjectmodel_1.IXpsDocumentPackageTarget.GetXpsOMPackageWriter
title: IXpsDocumentPackageTarget::GetXpsOMPackageWriter
author: windows-sdk-content
description: Gets the IXpsOMPackageWriter object for the document package.
old-location: xps\ixpsdocumentpackagetarget_getxpsompackagewriter.htm
old-project: printdocs
ms.assetid: D20AE05F-466F-44B6-972A-06AA872FF7BA
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetXpsOMPackageWriter, GetXpsOMPackageWriter method [XPS Documents and Packaging], GetXpsOMPackageWriter method [XPS Documents and Packaging],IXpsDocumentPackageTarget interface, IXpsDocumentPackageTarget interface [XPS Documents and Packaging],GetXpsOMPackageWriter method, IXpsDocumentPackageTarget.GetXpsOMPackageWriter, IXpsDocumentPackageTarget::GetXpsOMPackageWriter, xps.ixpsdocumentpackagetarget_getxpsompackagewriter, xpsobjectmodel_1/IXpsDocumentPackageTarget::GetXpsOMPackageWriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel_1.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Xpsobjectmodel_1.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_DOCUMENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xpsobjectmodel_1.h
api_name:
 - IXpsDocumentPackageTarget.GetXpsOMPackageWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsDocumentPackageTarget::GetXpsOMPackageWriter


## -description


Gets the <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> object for the document package.


## -parameters




### -param documentSequencePartName [in]

The document sequence part name.


### -param discardControlPartName [in]

The control part name.


### -param packageWriter [out, retval]

The <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> object.


## -returns



This method returns an HRESULT value. If the method call fails, it returns the appropriate HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/B8B43CE5-2222-428B-8E78-C7049D027EE1">IXpsDocumentPackageTarget</a>



<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>
 

 

