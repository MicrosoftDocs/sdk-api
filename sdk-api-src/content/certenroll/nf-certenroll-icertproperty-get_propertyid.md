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

# ICertProperty::get_PropertyId


## -description


The <b>PropertyId</b> property specifies or retrieves a value of the <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> enumeration that identifies an external  certificate property.

This property is read/write.


## -parameters


## -remarks



 Call the <b>PropertyId</b> property before trying to initialize the <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a> object. Call the <a href="https://msdn.microsoft.com/38b51242-cd4a-402e-b7ff-286f7bf66953">InitializeDecode</a> method or the <a href="https://msdn.microsoft.com/5d23bacc-bbe5-42fa-b4c5-57a6767f79ba">InitializeFromCertificate</a> method to create a value for the certificate property. Call the <a href="https://msdn.microsoft.com/1413f6da-0fcf-42ca-a79f-43f164368407">RawData</a> property to retrieve the property value.




## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

