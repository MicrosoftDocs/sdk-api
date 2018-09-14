---
UID: NF:xpsobjectmodel.IXpsOMDocumentStructureResource.GetOwner
title: IXpsOMDocumentStructureResource::GetOwner
author: windows-sdk-content
description: Gets a pointer to the IXpsOMDocument interface that contains the resource.
old-location: xps\ixpsomdocumentstructureresource_getowner.htm
tech.root: printdocs
ms.assetid: cbaedef0-f1a9-4c2c-88ae-1542cfbff252
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMDocumentStructureResource interface, IXpsOMDocumentStructureResource interface [XPS Documents and Packaging],GetOwner method, IXpsOMDocumentStructureResource.GetOwner, IXpsOMDocumentStructureResource::GetOwner, xps.ixpsomdocumentstructureresource_getowner, xpsobjectmodel/IXpsOMDocumentStructureResource::GetOwner
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - xpsobjectmodel.h
api_name:
 - IXpsOMDocumentStructureResource.GetOwner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDocumentStructureResource::GetOwner


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface that contains the resource.


## -parameters




### -param owner [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface that contains the resource. If the resource is not part of a document, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a>



<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

