---
UID: NN:shobjidl_core.IThumbnailHandlerFactory
title: IThumbnailHandlerFactory
author: windows-sdk-content
description: Exposes a method for retrieving the thumbnail handler of an item. Implement this interface if you want to specify what extractor is used for a child IDList.
old-location: shell\IThumbnailHandlerFactory.htm
tech.root: shell
ms.assetid: 83a9f676-ba03-4a0b-abe6-65f70c8babac
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IThumbnailHandlerFactory, IThumbnailHandlerFactory interface [Windows Shell], IThumbnailHandlerFactory interface [Windows Shell],described, _shell_IThumbnailHandlerFactory, shell.IThumbnailHandlerFactory, shobjidl_core/IThumbnailHandlerFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IThumbnailHandlerFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IThumbnailHandlerFactory interface


## -description


Exposes a method for retrieving the thumbnail handler of an item. Implement this interface if you want to specify what extractor is used for a child IDList.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThumbnailHandlerFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IThumbnailHandlerFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IThumbnailHandlerFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddd0caba-079f-4b22-8c89-6ba09adeba60">GetThumbnailHandler</a>
</td>
<td align="left" width="63%">
Gets the requested thumbnail handler for the thumbnail of a given item.

</td>
</tr>
</table> 

