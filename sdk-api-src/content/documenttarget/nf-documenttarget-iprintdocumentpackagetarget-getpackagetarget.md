---
UID: NF:documenttarget.IPrintDocumentPackageTarget.GetPackageTarget
title: IPrintDocumentPackageTarget::GetPackageTarget
author: windows-sdk-content
description: Retrieves the pointer to the specific document package target, which allows the client to add a document with the given target type. Clients can call this method multiple times but they always have to use the same target ID.
old-location: xps\iprintdocumentpackagetarget_getpackagetarget.htm
tech.root: printdocs
ms.assetid: 7D9A749D-954E-43BA-A522-98CBAD79D18C
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetPackageTarget, GetPackageTarget method [XPS Documents and Packaging], GetPackageTarget method [XPS Documents and Packaging],IPrintDocumentPackageTarget interface, IPrintDocumentPackageTarget interface [XPS Documents and Packaging],GetPackageTarget method, IPrintDocumentPackageTarget.GetPackageTarget, IPrintDocumentPackageTarget::GetPackageTarget, documenttarget/IPrintDocumentPackageTarget::GetPackageTarget, xps.iprintdocumentpackagetarget_getpackagetarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: documenttarget.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Documenttarget.h
api_name:
 - IPrintDocumentPackageTarget.GetPackageTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- documenttarget.h
: 
- IPrintDocumentPackageTarget.GetPackageTarget
: 
---

# IPrintDocumentPackageTarget::GetPackageTarget


## -description


Retrieves the pointer to the specific document package target, which allows the client to add a document with the given target type. Clients can call this method multiple times but they always have to use  the same target ID.


## -parameters




### -param guidTargetType [in]

The target type GUID obtained from <a href="https://msdn.microsoft.com/2875B751-0D49-4CFC-AF96-7009400E5D6E">GetPackageTargetTypes</a>.


### -param riid [in]

The identifier of the interface being requested.


### -param ppvTarget [out]

The requested document target interface. The returned pointer is a pointer to an <a href="https://msdn.microsoft.com/B8B43CE5-2222-428B-8E78-C7049D027EE1">IXpsDocumentPackageTarget</a> interface.


## -returns



If the <b>GetPackageTarget</b> method completes successfully, it returns an S_OK. Otherwise it returns the appropriate HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/0F63C626-DB58-4952-BBB3-7E3901429C35">IPrintDocumentPackageTarget</a>
 

 

