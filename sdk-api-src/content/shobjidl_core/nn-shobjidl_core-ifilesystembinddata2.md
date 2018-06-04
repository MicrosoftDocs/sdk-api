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

# IFileSystemBindData2 interface


## -description


Extends <a href="https://msdn.microsoft.com/f5099bb3-21a7-4708-ac48-d32a14646614">IFileSystemBindData</a>, which stores file system information for optimizing calls to <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a>. This interface adds the ability set or get file ID or junction class identifier (CLSID).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemBindData2</b> interface inherits from <a href="https://msdn.microsoft.com/f5099bb3-21a7-4708-ac48-d32a14646614">IFileSystemBindData</a>. <b>IFileSystemBindData2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemBindData2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77052ae5-d663-4bf8-967a-29bd5dc85706">GetFileID</a>
</td>
<td align="left" width="63%">
Gets the unique file identifier for the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57c5205a-9a56-4c47-bec4-11a690107bc6">GetJunctionCLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID of the object that implements <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> for the item, if the item is a junction point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3da2a22-cd45-4f3f-afcc-183a20f60f15">SetFileID</a>
</td>
<td align="left" width="63%">
Sets the unique file identifier for the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e072818d-dfa4-4b95-93b6-275206596147">SetJunctionCLSID</a>
</td>
<td align="left" width="63%">
Sets the CLSID of the object that implements <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>, if the current item is a junction point.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/f5099bb3-21a7-4708-ac48-d32a14646614">IFileSystemBindData</a> interface, from which it inherits.

To pass the information expressed in this interface to a data source <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a>, an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> object is created (use <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a>) and populated with an object that implements <a href="https://msdn.microsoft.com/f5099bb3-21a7-4708-ac48-d32a14646614">IFileSystemBindData</a> by calling the following:
  

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IBindCtx::RegisterObjectParam(STR_FILE_SYS_BIND_DATA, pfsbd)
</pre>
</td>
</tr>
</table></span></div>
 Where <i>pfsbd</i> is the object that implements <b>IFileSystemBindData</b>.

Implementers of <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a> first make the following call.
              

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IUnknown *punk;
pbc-&gt;GetObjectParam(STR_FILE_SYS_BIND_DATA, &amp;punk);
</pre>
</td>
</tr>
</table></span></div>
 Next the implementer calls one of the <b>Get</b> methods listed above to retrieve the parameters.
            



