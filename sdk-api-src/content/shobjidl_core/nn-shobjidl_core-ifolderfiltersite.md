---
UID: NN:shobjidl_core.IFolderFilterSite
title: IFolderFilterSite
author: windows-sdk-content
description: Exported by a host to allow clients to specify how to filter a Shell folder enumeration.
old-location: shell\IFolderFilterSite.htm
tech.root: shell
ms.assetid: 8b6fe1a3-9977-42a8-af95-da0fc6809b1b
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IFolderFilterSite, IFolderFilterSite interface [Windows Shell], IFolderFilterSite interface [Windows Shell],described, _shell_IFolderFilterSite, shell.IFolderFilterSite, shobjidl_core/IFolderFilterSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFolderFilterSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFolderFilterSite interface


## -description


Exported by a host to allow clients to specify how to filter a Shell folder enumeration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderFilterSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFolderFilterSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFolderFilterSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bbcb238-9b3e-4f5c-9cb3-429d0ff918af">SetFilter</a>
</td>
<td align="left" width="63%">
Exposed by a host to allow clients to pass the host their <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointers.

</td>
</tr>
</table> 


## -remarks



The most common use of this interface is when your application calls <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a>. When you call this function, you become a client of the folder browser object. That object communicates with you by sending messages to a callback function, <a href="https://msdn.microsoft.com/e9109f38-34c7-46c0-aa0c-a6b4570f1c3a">BrowseCallbackProc</a>. The BFFM_IUNKNOWN message contains a pointer to the folder browser's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. To filter folder enumeration:



<ol>
<li>Use the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer to call the folder browser's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method, and request a pointer to the <b>IFolderFilterSite</b> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/1bbcb238-9b3e-4f5c-9cb3-429d0ff918af">IFolderFilterSite::SetFilter</a>, and pass the folder browser a pointer to your <a href="https://msdn.microsoft.com/fd69c11c-f4c3-4681-ae85-385460e96be9">IFolderFilter</a> (IUnknown or IFilterFolder?) interface.</li>
<li>The folder browser will then query the two methods of the <b>IFolderFilterSite</b> interface to determine how to filter the enumeration.</li>
</ol>


