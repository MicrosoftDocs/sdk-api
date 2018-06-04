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

# tagFailureCategoryMapping structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>FailureCategoryMapping</b> structure contains optional compliance state information that is returned by the System Health Validator (SHV).


## -struct-fields




### -field mappingCompliance

An array of        <b>BOOLs</b> that contain the compliance state of each <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">FailureCategory</a>.  <b>TRUE</b> indicates the category is compliant and <b>FALSE</b> indicates non-compliance. 

<div class="alert"><b>Note</b>  The length of <b>mappingCompliance</b> is defined by <a href="https://msdn.microsoft.com/2727487c-8c6a-4cd9-b6d8-253191a7d7f6">failureCategoryCount</a>.</div>
<div> </div>

## -remarks



If a failure occurs in the system (for example, a component or communication failures), the SHV may return
   an <a href="https://msdn.microsoft.com/ba725bf1-1d0a-4489-b912-3e761557d772">sohAttributeTypeFailureCategory</a> type type-length-value (TLV) object in its <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoHResponse</a> instead
   of making a compliance decision. In turn, the NAP system maps the <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">FailureCategory</a> type returned by the TLV object to compliant or non-compliant within the <b>FailureCategoryMapping</b> structure as follows:

<ul>
<li>mappingCompliance[0] = mapping for <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">failureCategoryOther</a>
</li>
<li>mappingCompliance[1] = mapping for <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">failureCategoryClientComponent</a>
</li>
<li>mappingCompliance[2] = mapping for <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">failureCategoryClientCommunication</a>
</li>
<li>mappingCompliance[3] = mapping for <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">failureCategoryServerComponent</a>
</li>
<li>mappingCompliance[4] = mapping for <a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">failureCategoryServerCommunication</a>
</li>
</ul>
By default, all categories map to non-compliant (FALSE).




## -see-also




<a href="https://msdn.microsoft.com/3f528702-c9f3-4a91-960b-8b3f3eea91e9">FailureCategory</a>
 

 

