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

# ITfMSAAControl interface


## -description


The <b>ITfMSAAControl</b> interface is used by <a href="_msaa_microsoft_active_accessibility_start_page">Microsoft Active Accessibility</a> to add or remove a document from TSF control, to avoid unnecessary overhead in TSF. This interface is not recommended for use by other applications.

The interface ID is IID_ITfMSAAControl.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMSAAControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfMSAAControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMSAAControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/344cabbb-286e-415d-980f-349fb637a78d">SystemDisableMSAA</a>
</td>
<td align="left" width="63%">
Used by MSAA to halt TSF support of an MSAA client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fec3aa3f-3554-4c21-9557-a12388d97a94">SystemEnableMSAA</a>
</td>
<td align="left" width="63%">
Used by MSAA to request TSF support of an MSAA client.

</td>
</tr>
</table> 


## -see-also




<a href="_COM_IUnknown">IUnknown</a>



<a href="_msaa_microsoft_active_accessibility_start_page">Microsoft Active Accessibility</a>
 

 

