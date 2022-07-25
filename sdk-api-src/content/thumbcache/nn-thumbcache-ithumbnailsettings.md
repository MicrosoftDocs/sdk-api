---
UID: NN:thumbcache.IThumbnailSettings
title: IThumbnailSettings (thumbcache.h)
description: Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request.
helpviewer_keywords: ["IThumbnailSettings","IThumbnailSettings interface [Windows Shell]","IThumbnailSettings interface [Windows Shell]","described","shell.IThumbnailSettings","thumbcache/IThumbnailSettings"]
old-location: shell\IThumbnailSettings.htm
tech.root: shell
ms.assetid: 502537E5-1D72-44f0-BC75-DBED61F174FC
ms.date: 12/05/2018
ms.keywords: IThumbnailSettings, IThumbnailSettings interface [Windows Shell], IThumbnailSettings interface [Windows Shell],described, shell.IThumbnailSettings, thumbcache/IThumbnailSettings
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IThumbnailSettings
 - thumbcache/IThumbnailSettings
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
 - IThumbnailSettings
---

# IThumbnailSettings interface


## -description

Provides a method that enables a thumbnail provider to determine the user context of a thumbnail request.

## -inheritance

The <b>IThumbnailSettings</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IThumbnailSettings</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
This interface can be implemented by any thumbnail provider that supports <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a> or <a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailprovider">IThumbnailProvider</a>.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
