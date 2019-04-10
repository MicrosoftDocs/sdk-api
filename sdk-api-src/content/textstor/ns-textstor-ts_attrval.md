---
UID: NS:textstor.TS_ATTRVAL
title: TS_ATTRVAL (textstor.h)
author: windows-sdk-content
description: The TS_ATTRVAL structure contains document attribute values.
old-location: tsf\ts_attrval.htm
tech.root: TSF
ms.assetid: 9209ef60-6a1d-4aad-9f9f-775534116f37
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TS_ATTRVAL, TS_ATTRVAL structure [Text Services Framework], _tsf_ts_attrval_ref, textstor/TS_ATTRVAL, tsf.ts_attrval
ms.topic: struct
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TS_ATTRVAL
product: Windows
targetos: Windows
req.typenames: TS_ATTRVAL
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TS_ATTRVAL structure


## -description



The <b>TS_ATTRVAL</b> structure contains document attribute values.




## -struct-fields




### -field idAttr

GUID for the attribute type.


### -field dwOverlapId

A unique identifier of this attribute when overlapped with other attributes. This is a feature in <a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Microsoft Active Accessibility</a>. In TSF, this parameter value is zero (0). Any nonzero value is ignored.


### -field varValue

Value of the attribute.


## -remarks



An application uses attributes to expose its data to TSF, whereas text services use properties to expose their data to TSF. <b>TS_ATTRVAL</b> is used in <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> and <a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/ffd27e9b-3281-45a9-84f2-d09103689ced">ITextStoreACP::RequestAttrsTransitioningAtPosition
      </a>



<a href="https://msdn.microsoft.com/243cd002-c882-4ce9-b528-1a2229c46f4a">ITextStoreACP::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/6cd34ca5-6561-4161-beac-98248f0415f6">ITextStoreACP::RetrieveRequestedAttrs
      </a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/f0f43237-8c26-4e0c-8717-908884229b7b">ITextStoreAnchor::RequestAttrsTransitioningAtPosition
      </a>



<a href="https://msdn.microsoft.com/ab81d79d-e991-4c2d-9fb7-95393e002828">ITextStoreAnchor::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Microsoft Active Accessibility</a>



<a href="https://msdn.microsoft.com/50a5930c-ba17-4441-99a7-efc6c4bfc2ab">TF_PROPERTYVAL
      </a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID
      </a>
 

 

