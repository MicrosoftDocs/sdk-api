---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePackageFromFile1
title: IXpsOMObjectFactory1::CreatePackageFromFile1 method
author: windows-driver-content
description: Opens an XPS package file and returns an instantiated XPS document object tree. This method will read a file that contains an XPS document that is of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS.
old-location: xps\ixpsomobjectfactory1_createpackagefromfile1.htm
old-project: printdocs
ms.assetid: c5641576-9280-48a5-9fb6-ef3d2811386a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreatePackageFromFile1 method [XPS Documents and Packaging], CreatePackageFromFile1 method [XPS Documents and Packaging], IXpsOMObjectFactory1 interface, CreatePackageFromFile1,IXpsOMObjectFactory1.CreatePackageFromFile1, IXpsOMObjectFactory1, IXpsOMObjectFactory1 interface [XPS Documents and Packaging], CreatePackageFromFile1 method, IXpsOMObjectFactory1::CreatePackageFromFile1, xps.ixpsomobjectfactory1_createpackagefromfile1, xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageFromFile1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_DOCUMENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	none
-	none.dll
api_name:
-	IXpsOMObjectFactory1.CreatePackageFromFile1
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory1::CreatePackageFromFile1 method


## -description


Opens an XPS package file and returns an instantiated XPS document object tree. This method will read a file that contains an XPS document that is of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS


## -parameters




### -param filename

[in, string] The name of the XPS package file.


### -param reuseObjects

[in]            The Boolean value that indicates that the software is to attempt to optimize the document object tree by sharing objects that are identical in all properties and children. 

TRUE: The software will attempt to optimize the object tree.

FALSE: The software will not attempt to optimize the object tree.


### -param package






#### - Package

[out, retval]   A pointer to the new IXpsOMPackage1 interface that contains the XPS document object tree that was read from filename.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The method succeeded. 

XPS_E_UNEXPECTED_NAMESPACE: The package markup uses a namespace that is not supported by the document type

XPS_E_ABSOLUTE_REFERENCE: The OpenXPS document contains XML elements that use absolute URIs to reference other parts in the document. 




## -remarks



Use this method to read a file that contains an XPS document that could be of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS.   <a href="https://msdn.microsoft.com/2498792b-a33c-47cd-8d88-8e89b99c432d">CreatePackageFromFile</a>, released in Windows 7, only opens files that contain an XPS document of type XPS_DOCUMENT_TYPE_ XPS.




## -see-also




<a href="https://msdn.microsoft.com/f013e59d-83ae-453f-9cc5-9a8230729128">IXpsOMObjectFactory1</a>
 

 

