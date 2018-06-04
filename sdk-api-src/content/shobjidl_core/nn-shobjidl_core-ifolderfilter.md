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

# IFolderFilter interface


## -description


Exposed by a client to specify how to filter the enumeration of a Shell folder by a server application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFolderFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFolderFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b02b103c-b82e-455b-9498-dfc387806c36">GetEnumFlags</a>
</td>
<td align="left" width="63%">
Allows a client to specify which classes of objects in a Shell folder should be enumerated. When used with <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a>, specifies the class or classes of items that should be shown in the dialog box tree view and which class or classes should not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60893b97-5b13-4c1f-9fd6-042217d3026f">ShouldShow</a>
</td>
<td align="left" width="63%">
Specifies whether an individual item should be allowed through the filter and which should be blocked. When used with <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a>, specifies which items should be shown in the dialog box tree view and which should not. The determination to show or not show an item is up to the application.

</td>
</tr>
</table> 


## -remarks



This interface is most often used with <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a> to filter the contents of the tree view displayed in a folder selection dialog box. To use <b>IFolderFilter</b> with <b>SHBrowseForFolder</b>, the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BIF_NEWDIALOGSTYLE</a> flag must be set.

When your application calls <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a>, you become a client of the folder browser object. The folder browser object communicates with you by sending messages to a callback function, <a href="https://msdn.microsoft.com/e9109f38-34c7-46c0-aa0c-a6b4570f1c3a">BrowseCallbackProc</a>. The <b>BFFM_IUNKNOWN</b> message handled by that callback function contains a pointer to the folder browser's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. To filter the display of a folder's contents, do the following:

                

<ol>
<li>Use the folder browser's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method to request a pointer to the <a href="https://msdn.microsoft.com/8b6fe1a3-9977-42a8-af95-da0fc6809b1b">IFolderFilterSite</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/1bbcb238-9b3e-4f5c-9cb3-429d0ff918af">IFolderFilterSite::SetFilter</a>, passing it a pointer to your <b>IFolderFilter</b> interface.</li>
<li>The folder browser then queries <a href="https://msdn.microsoft.com/b02b103c-b82e-455b-9498-dfc387806c36">IFolderFilter::GetEnumFlags</a> and <a href="https://msdn.microsoft.com/60893b97-5b13-4c1f-9fd6-042217d3026f">IFolderFilter::ShouldShow</a>to determine how to filter the enumeration.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/8b6fe1a3-9977-42a8-af95-da0fc6809b1b">IFolderFilterSite</a>
 

 

