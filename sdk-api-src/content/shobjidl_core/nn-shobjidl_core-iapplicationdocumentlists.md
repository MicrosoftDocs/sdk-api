---
UID: NN:shobjidl_core.IApplicationDocumentLists
title: IApplicationDocumentLists
author: windows-sdk-content
description: Exposes methods that allow an application to retrieve the contents of the Recent or Frequent categories in a Jump List.
old-location: shell\IApplicationDocumentLists.htm
old-project: shell
ms.assetid: 1912d8fd-1724-4a4b-b74a-e05db12ffead
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IApplicationDocumentLists, IApplicationDocumentLists interface [Windows Shell], IApplicationDocumentLists interface [Windows Shell],described, _shell_IApplicationDocumentLists, shell.IApplicationDocumentLists, shobjidl_core/IApplicationDocumentLists
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IApplicationDocumentLists
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IApplicationDocumentLists interface


## -description


Exposes methods that allow an application to retrieve the contents of the <b>Recent</b> or <b>Frequent</b> categories in a Jump List.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationDocumentLists</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IApplicationDocumentLists</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationDocumentLists</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d86bf039-81d9-4d43-9671-b107d7e925ab">GetList</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents the collection of destinations listed in the <b>Recent</b> or <b>Frequent</b> category in a Jump List.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c5135c1-b98d-4d27-8437-5ca57af9a525">SetAppID</a>
</td>
<td align="left" width="63%">
Specifies a unique AppUserModelID for the application whose destination lists are being retrieved. This method is optional.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_ApplicationDocumentLists. This interface is not implemented by third parties.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
An application calls the methods of this interface when it wants to retrieve a Jump List's <b>Recent</b> or <b>Frequent</b> list. These lists are generated through calls to <a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a>, either explicitly or by the system when a file is opened through Windows Explorer or the common file dialog is used to open, save, or create a file.



<b>IApplicationDocumentLists</b> is used only with the automatically generated <b>Recent</b> or <b>Frequent</b> categories. It cannot retrieve a list of items that the user has pinned to the Jump List. That list cannot be retrieved programmatically because it cannot be manipulated programmatically; it is strictly under the user's control. <b>IApplicationDocumentLists</b> also cannot access custom categories or the task list.




## -see-also




<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

