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

# ITextStoreACP::RetrieveRequestedAttrs


## -description


Gets the attributes returned by a call to an attribute request method.


## -parameters




### -param ulCount [in]

Specifies the number of supported attributes to obtain.


### -param paAttrVals [out]

Pointer to the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure that receives the supported attributes. The members of this structure depend upon the <i>dwFlags</i> parameter of the calling method.


### -param pcFetched [out]

Receives the number of supported attributes.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/39eb59cd-ec55-4057-8cf1-0203b6e6c82b">ITextStoreACP::RequestAttrsAtPosition
      </a>



<a href="https://msdn.microsoft.com/243cd002-c882-4ce9-b528-1a2229c46f4a">
        ITextStoreACP::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">
        TS_ATTRVAL
      </a>



<a href="https://msdn.microsoft.com/ffd27e9b-3281-45a9-84f2-d09103689ced">
        TextStoreACP::RequestAttrsTransitioningAtPosition
      </a>
 

 

