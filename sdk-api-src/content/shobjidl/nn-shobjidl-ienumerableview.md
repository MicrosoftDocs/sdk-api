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

# IEnumerableView interface


## -description


Exposes methods that enumerate the contents of a view and receive notification from callback upon enumeration completion. This interface enables clients of a view to attempt to share the view's list of folder contents.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumerableView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumerableView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumerableView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/413d913d-e6f3-4e2d-bf1f-5d5ad6d4f650">CreateEnumIDListFromContents</a>
</td>
<td align="left" width="63%">
Creates an enumerator of ID lists from the contents of the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af824c16-5bbf-4c75-88d0-b76519152360">SetEnumReadyCallback</a>
</td>
<td align="left" width="63%">
Sets a callback on the view that is notified when the initial view enumeration is complete.

</td>
</tr>
</table> 


## -remarks




<a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a> (a folder view) supports presentation of the contents of a folder, and exposes the <b>IEnumerableView</b> through <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> on service request SID_EnumerableView. <b>IEnumerableView</b> offers enhanced performance compared to obtaining the contents of the folder directly from the folder using <a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a> (call <a href="https://msdn.microsoft.com/248bec8b-0bf4-47d5-adb3-31a685a2c359">IShellFolder::EnumObjects</a> to return this interface). Since the view asked for the contents of the folder in order to display those contents, using <b>IEnumerableView</b> enables a client to get a copy of the work already done by <b>IFolderView</b>.

Typicallly, this enumeration service is compatible with most folders, and is only provided if it is safe to enumerate the contents of the view.  For example, using this service with a folder containing search results is not supported.
          



