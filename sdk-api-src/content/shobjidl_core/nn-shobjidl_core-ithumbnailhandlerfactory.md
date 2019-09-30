---
UID: NN:shobjidl_core.IThumbnailHandlerFactory
title: IThumbnailHandlerFactory (shobjidl_core.h)
author: windows-sdk-content
description: Exposes a method for retrieving the thumbnail handler of an item. Implement this interface if you want to specify what extractor is used for a child IDList.
old-location: shell\IThumbnailHandlerFactory.htm
tech.root: shell
ms.assetid: 83a9f676-ba03-4a0b-abe6-65f70c8babac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IThumbnailHandlerFactory, IThumbnailHandlerFactory interface [Windows Shell], IThumbnailHandlerFactory interface [Windows Shell],described, _shell_IThumbnailHandlerFactory, shell.IThumbnailHandlerFactory, shobjidl_core/IThumbnailHandlerFactory
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IThumbnailHandlerFactory"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IThumbnailHandlerFactory interface


## -description


Exposes a method for retrieving the thumbnail handler of an item. Implement this interface if you want to specify what extractor is used for a child IDList.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThumbnailHandlerFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IThumbnailHandlerFactory</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ithumbnailhandlerfactory-getthumbnailhandler">GetThumbnailHandler</a>
</td>
<td align="left" width="63%">
Gets the requested thumbnail handler for the thumbnail of a given item.

</td>
</tr>
</table> 

