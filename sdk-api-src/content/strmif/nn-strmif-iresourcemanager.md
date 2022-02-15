---
UID: NN:strmif.IResourceManager
title: IResourceManager (strmif.h)
description: The IResourceManager interface resolves contentions for system resources.The filter graph manager exposes this interface.
helpviewer_keywords: ["IResourceManager","IResourceManager interface [DirectShow]","IResourceManager interface [DirectShow]","described","IResourceManagerInterface","dshow.iresourcemanager","strmif/IResourceManager"]
old-location: dshow\iresourcemanager.htm
tech.root: dshow
ms.assetid: 8cbe908e-5675-4134-81e7-2c5c31b0ffc5
ms.date: 12/05/2018
ms.keywords: IResourceManager, IResourceManager interface [DirectShow], IResourceManager interface [DirectShow],described, IResourceManagerInterface, dshow.iresourcemanager, strmif/IResourceManager
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResourceManager
 - strmif/IResourceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceManager
---

# IResourceManager interface


## -description

The <code>IResourceManager</code> interface resolves contentions for system resources.

The filter graph manager exposes this interface. Filters can use this interface to request resources that other objects are likely to use. For example, audio renderers use this interface to resolve contentions for the wave-output device, to enable sound to follow focus.

Applications will typically not use this interface.

An object can use this interface to resolve possible contentions between existing resources. The object registers the resource with the interface and then requests it whenever needed. The object should notify the filter graph manager whenever the user focus changes. The filter graph manager can then switch contended resources to the objects that have the focus of the user.

An object that uses this interface must implement the <a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> interface. <b>IResourceConsumer</b> provides a callback mechanism for the filter graph manager to notify the object when a resource becomes available, or when the object should release a resource that it acquired.

## -inheritance

The <b>IResourceManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResourceManager</b> also has these types of members:

