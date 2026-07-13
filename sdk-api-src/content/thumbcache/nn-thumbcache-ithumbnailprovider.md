---
UID: NN:thumbcache.IThumbnailProvider
title: IThumbnailProvider (thumbcache.h)
description: Exposes a method for getting a thumbnail image and is intended to be implemented for thumbnail handlers. The object that implements this interface must also implement IInitializeWithStream.
helpviewer_keywords: ["IThumbnailProvider","IThumbnailProvider interface [Windows Shell]","IThumbnailProvider interface [Windows Shell]","described","_shell_IThumbnailProvider","shell.IThumbnailProvider","thumbcache/IThumbnailProvider"]
old-location: shell\IThumbnailProvider.htm
tech.root: shell
ms.assetid: 55c4739a-4835-4f53-a435-804ddf06ffcf
ms.date: 01/22/2025
ms.keywords: IThumbnailProvider, IThumbnailProvider interface [Windows Shell], IThumbnailProvider interface [Windows Shell],described, _shell_IThumbnailProvider, shell.IThumbnailProvider, thumbcache/IThumbnailProvider
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IThumbnailProvider
 - thumbcache/IThumbnailProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - IThumbnailProvider
---

# IThumbnailProvider interface


## -description

Exposes a method for getting a thumbnail image and is intended to be implemented for thumbnail handlers. The object that implements this interface must also implement <a href="/windows/desktop/api/propsys/nn-propsys-iinitializewithstream">IInitializeWithStream</a>.

## -inheritance

The <b>IThumbnailProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IThumbnailProvider</b> also has these types of members:

## -remarks

The Shell calls <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail">IThumbnailProvider::GetThumbnail</a> to obtain an image to use as a representation of the item.

An implementation of this interface for photo thumbnails is supplied in Microsoft Windows as CLSID_PhotoThumbnailProvider. Applications that use the supplied implementation must define a constant CLSID identifier using the GUID {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}.
				


```
// {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
const CLSID CLSID_PhotoThumbnailProvider = {0xC7657C4A, 0x9F68, 0x40fa, {0xA4, 0xDF, 0x96, 0xBC, 0x08, 0xEB, 0x35, 0x51}} ;
```


<b>Initializing</b> The object that implements this interface must also implement <a href="/windows/desktop/api/propsys/nn-propsys-iinitializewithstream">IInitializeWithStream</a>. The Shell calls <a href="/windows/desktop/api/propsys/nf-propsys-iinitializewithstream-initialize">IInitializeWithStream::Initialize</a> with the stream of the item, and  <b>IInitializeWithStream</b> is the only initialization interface used when IThumbnailProvider instances are loaded out-of-proc (for isolation purposes).  This is the primary code path for Windows  for all IThumbnailCache code paths.

It is possible for a thumbnail implementation to be initialized with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem">IInitializeWithItem</a> or <a href="/windows/desktop/api/propsys/nn-propsys-iinitializewithfile">IInitializeWithFile</a> when the handler is request by a 3rd party without using the IThumbnailCache API, but this is uncommon.  If you implement <b>IInitializeWithItem</b>, the Shell calls <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize">IInitializeWithItem::Initialize</a> with the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> representation of the item. If you implement <b>IInitializeWithFile</b>, the Shell calls <a href="/windows/desktop/api/propsys/nf-propsys-iinitializewithfile-initialize">IInitializeWithFile::Initialize</a> with the path of the file.

If none of these interfaces is present, <b>IThumbnailProvider</b> is not called.

<b>Client apps</b> If you're developing a client app, you should use <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory">IShellItemImageFactory</a> instead. 

<b>Windows Vista</b> IThumbnailProvider is new for Vista and replaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a>. Vista still supports IExtractImage but lacks the ability to return the image type (alpha or not).
