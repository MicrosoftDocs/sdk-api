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

# ILoadFilter interface


## -description


Defines methods and properties that are implemented by the FilterRegistration object, which provides methods for loading a filter.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILoadFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILoadFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILoadFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/920c976e-4dde-4e53-85b7-7547291736a0"> LoadIFilter</a>
</td>
<td align="left" width="63%">
Registers the filters that need to be mapped to the CLSID (CLSID_FilterRegistration), file name extensions, and MIME types that identify the content type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4eff132-9022-4091-a2a3-1d8e11a35b39">LoadIFilterFromStorage</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a577306-d5ff-43c1-ab9f-3a7437661d2a">LoadIFilterFromStream</a>
</td>
<td align="left" width="63%">
This method is not implemented.

</td>
</tr>
</table> 


## -remarks



A filter, also known as a filter handler, is an implementation of the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> interface.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7b24986b-972d-4674-846b-f856b908edf4">Developing Filter Handlers</a>



<a href="https://msdn.microsoft.com/5baae290-aead-4986-a7d4-0302931e0104">FILTERED_DATA_SOURCES</a>



<a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>



<b>Reference</b>
 

 

