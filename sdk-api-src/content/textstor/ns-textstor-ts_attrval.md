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

# TS_ATTRVAL structure


## -description



The <b>TS_ATTRVAL</b> structure contains document attribute values.




## -struct-fields




### -field idAttr

GUID for the attribute type.


### -field dwOverlapId

A unique identifier of this attribute when overlapped with other attributes. This is a feature in <a href="_msaa_microsoft_active_accessibility_start_page">Microsoft Active Accessibility</a>. In TSF, this parameter value is zero (0). Any nonzero value is ignored.


### -field varValue

Value of the attribute.


## -remarks



An application uses attributes to expose its data to TSF, whereas text services use properties to expose their data to TSF. <b>TS_ATTRVAL</b> is used in <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> and <a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">
        ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/ffd27e9b-3281-45a9-84f2-d09103689ced">ITextStoreACP::RequestAttrsTransitioningAtPosition
      </a>



<a href="https://msdn.microsoft.com/243cd002-c882-4ce9-b528-1a2229c46f4a">
        ITextStoreACP::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/6cd34ca5-6561-4161-beac-98248f0415f6">
        ITextStoreACP::RetrieveRequestedAttrs
      </a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">
        ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/f0f43237-8c26-4e0c-8717-908884229b7b">
        ITextStoreAnchor::RequestAttrsTransitioningAtPosition
      </a>



<a href="https://msdn.microsoft.com/ab81d79d-e991-4c2d-9fb7-95393e002828">
        ITextStoreAnchor::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">
        ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="_msaa_microsoft_active_accessibility_start_page">Microsoft Active Accessibility</a>



<a href="https://msdn.microsoft.com/50a5930c-ba17-4441-99a7-efc6c4bfc2ab">
        TF_PROPERTYVAL
      </a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">
        TS_ATTRID
      </a>
 

 

