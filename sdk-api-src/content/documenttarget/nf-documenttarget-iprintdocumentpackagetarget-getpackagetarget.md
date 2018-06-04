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
 

 

