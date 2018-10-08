---
UID: NN:thumbcache.IThumbnailProvider
title: IThumbnailProvider
author: windows-sdk-content
description: Exposes a method for getting a thumbnail image and is intended to be implemented for thumbnail handlers. The object that implements this interface must also implement IInitializeWithStream.
old-location: shell\IThumbnailProvider.htm
tech.root: shell
ms.assetid: 55c4739a-4835-4f53-a435-804ddf06ffcf
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IThumbnailProvider, IThumbnailProvider interface [Windows Shell], IThumbnailProvider interface [Windows Shell],described, _shell_IThumbnailProvider, shell.IThumbnailProvider, thumbcache/IThumbnailProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
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
 - Thumbcache.h
api_name:
 - IThumbnailProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IThumbnailProvider interface


## -description


Exposes a method for getting a thumbnail image and is intended to be implemented for thumbnail handlers. The object that implements this interface must also implement <a href="https://msdn.microsoft.com/9050845d-1e70-4e85-8d2f-c8bbb382abe5">IInitializeWithStream</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThumbnailProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IThumbnailProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IThumbnailProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ea237fb-6b1c-4e87-a9f3-711ffa37b3dc">GetThumbnail</a>
</td>
<td align="left" width="63%">
Gets a thumbnail image and alpha type.

</td>
</tr>
</table> 


## -remarks



The Shell calls <a href="https://msdn.microsoft.com/5ea237fb-6b1c-4e87-a9f3-711ffa37b3dc">IThumbnailProvider::GetThumbnail</a> to obtain an image to use as a representation of the item.

An implementation of this interface for photo thumbnails is supplied in Microsoft Windows as CLSID_PhotoThumbnailProvider. Applications that use the supplied implementation must define a constant CLSID identifier using the GUID {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}.
				


```
// {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
const CLSID CLSID_PhotoThumbnailProvider = {0xC7657C4A, 0x9F68, 0x40fa, {0xA4, 0xDF, 0x96, 0xBC, 0x08, 0xEB, 0x35, 0x51}} ;
```


<b>Initializing</b> The object that implements this interface must also implement <a href="https://msdn.microsoft.com/9050845d-1e70-4e85-8d2f-c8bbb382abe5">IInitializeWithStream</a>. The Shell calls <a href="https://msdn.microsoft.com/1e04c0a4-aa9b-4e2c-8307-525809ca903f">IInitializeWithStream::Initialize</a> with the stream of the item, and  <b>IInitializeWithStream</b> is the only initialization interface used when IThumbnailProvider instances are loaded out-of-proc (for isolation purposes).  This is the primary code path for Windows  for all IThumbnailCache code paths.

It is possible for a thumbnail implementation to be initialized with <a href="https://msdn.microsoft.com/95f3917e-66ca-45de-a3ed-811680a179e7">IInitializeWithItem</a> or <a href="https://msdn.microsoft.com/323181ab-1dc2-4b2a-a91f-3eccd7968bcd">IInitializeWithFile</a> when the handler is request by a 3rd party without using the IThumbnailCache API, but this is uncommon.  If you implement <b>IInitializeWithItem</b>, the Shell calls <a href="https://msdn.microsoft.com/61abf5c8-2847-4788-9d99-65f3b1c821d6">IInitializeWithItem::Initialize</a> with the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> representation of the item. If you implement <b>IInitializeWithFile</b>, the Shell calls <a href="https://msdn.microsoft.com/7b7bb534-dff7-455b-baee-f573fb645cc3">IInitializeWithFile::Initialize</a> with the path of the file.

If none of these interfaces is present, <b>IThumbnailProvider</b> is not called.

<b>Client apps</b> If you're developing a client app, you should use <a href="https://msdn.microsoft.com/a6eea412-553a-4bdd-afc2-cc002c4500a4">IShellItemImageFactory</a> instead. 

<b>Windows Vista</b> IThumbnailProivder is new for Vista and replaces <a href="https://msdn.microsoft.com/28a13749-89e7-407e-89cb-95464859ce3e">IExtractImage</a>. Vista still supports IExtractImage but lacks the ability to return the image type (alpha or not). 



