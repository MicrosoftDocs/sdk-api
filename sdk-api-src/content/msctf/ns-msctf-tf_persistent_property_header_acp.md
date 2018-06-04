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

# TF_PERSISTENT_PROPERTY_HEADER_ACP structure


## -description



The <b>TF_PERSISTENT_PROPERTY_HEADER_ACP</b> structure is used to provide property header data.




## -struct-fields




### -field guidType

Contains a GUID that identifies the property.


### -field ichStart

Contains the starting character position of the property.


### -field cch

Contains the number of characters that the property spans.


### -field cb

Contains the size, in bytes, of the property value.


### -field dwPrivate

Contains a <b>DWORD</b> value defined by the property owner.


### -field clsidTIP

Contains the CLSID of the property owner.


## -see-also




<a href="https://msdn.microsoft.com/14be52d1-4f8c-4deb-aa92-470c3608c841">
        ITextStoreACPServices::Serialize
      </a>



<a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">
        ITextStoreACPServices::Unserialize
      </a>



<a href="https://msdn.microsoft.com/e67b6fa7-610d-426f-a290-36c0da4068f4">ITfContextOwnerServices::Serialize
      </a>



<a href="https://msdn.microsoft.com/b02ffedf-83c5-48ff-8116-801aaec6dc71">
        ITfContextOwnerServices::Unserialize
      </a>



<a href="https://msdn.microsoft.com/20730a90-e59c-46ae-a0bf-a212b201351c">
        ITfPersistentPropertyLoaderACP::LoadProperty
      </a>
 

 

