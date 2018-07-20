---
UID: NS:msctf.TF_PERSISTENT_PROPERTY_HEADER_ACP
title: TF_PERSISTENT_PROPERTY_HEADER_ACP
author: windows-sdk-content
description: The TF_PERSISTENT_PROPERTY_HEADER_ACP structure is used to provide property header data.
old-location: tsf\tf_persistent_property_header_acp.htm
old-project: TSF
ms.assetid: 9c5cb193-d18e-4d91-b9be-b8a61a56d3a3
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: TF_PERSISTENT_PROPERTY_HEADER_ACP, TF_PERSISTENT_PROPERTY_HEADER_ACP structure [Text Services Framework], _tsf_tf_persistent_property_header_acp_ref, msctf/TF_PERSISTENT_PROPERTY_HEADER_ACP, tsf.tf_persistent_property_header_acp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_PERSISTENT_PROPERTY_HEADER_ACP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_PERSISTENT_PROPERTY_HEADER_ACP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

