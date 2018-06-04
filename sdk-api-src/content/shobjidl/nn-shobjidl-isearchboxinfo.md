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

# ISearchBoxInfo interface


## -description


Exposes methods that allow the caller to retrieve information entered into a search box.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchBoxInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchBoxInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchBoxInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a1159df-78ef-493b-8286-eefb0ac004ef">GetCondition</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the search box as an <a href="_search_ICondition">ICondition</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the search box as plain text.

</td>
</tr>
</table> 


## -remarks



The search box is shown here in an Windows Explorer window frame.



<img alt="Screen shot of upper-right corner of explorer frame showing search box" src="images/searchbox.jpg"/>
The frame that contains the search box might also be hosted in another window or in the common file dialog box.

To access the search dialog, use <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> using SID_SSearchBoxInfo on a site pointer within the Windows Explorer window.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided with Windows. Third parties do not need to implement their own version.



