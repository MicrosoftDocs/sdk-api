---
UID: NN:mfsharingengine.IPlayToSourceClassFactory
title: IPlayToSourceClassFactory (mfsharingengine.h)
description: Creates an instance of the PlayToSource object.
helpviewer_keywords: ["IPlayToSourceClassFactory","IPlayToSourceClassFactory interface [Media Foundation]","IPlayToSourceClassFactory interface [Media Foundation]","described","mf.iplaytocontrollerclassfactory","mf.iplaytosourceclassfactory","mfsharingengine/IPlayToSourceClassFactory"]
old-location: mf\iplaytosourceclassfactory.htm
tech.root: mf
ms.assetid: F8F9FEC6-836C-429A-BADD-5CD1E550AED0
ms.date: 12/05/2018
ms.keywords: IPlayToSourceClassFactory, IPlayToSourceClassFactory interface [Media Foundation], IPlayToSourceClassFactory interface [Media Foundation],described, mf.iplaytocontrollerclassfactory, mf.iplaytosourceclassfactory, mfsharingengine/IPlayToSourceClassFactory
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IPlayToSourceClassFactory
 - mfsharingengine/IPlayToSourceClassFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfsharingengine.h
api_name:
 - IPlayToSourceClassFactory
---

# IPlayToSourceClassFactory interface


## -description

Creates an instance of the <a href="/uwp/api/windows.media.playto.playtosource">PlayToSource</a> object.

## -inheritance

The <b>IPlayToSourceClassFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPlayToSourceClassFactory</b> also has these types of members:

## -remarks

To get a pointer to this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. The CLSID is <b>CLSID_PlayToSourceClassFactory</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
