---
UID: NF:mfsharingengine.IMFSharingEngineClassFactory.CreateInstance
title: IMFSharingEngineClassFactory::CreateInstance (mfsharingengine.h)
description: Creates an instance of the media sharing engine. (IMFSharingEngineClassFactory.CreateInstance)
helpviewer_keywords: ["CreateInstance","CreateInstance method [Media Foundation]","CreateInstance method [Media Foundation]","IMFSharingEngineClassFactory interface","IMFSharingEngineClassFactory interface [Media Foundation]","CreateInstance method","IMFSharingEngineClassFactory.CreateInstance","IMFSharingEngineClassFactory::CreateInstance","mf.imfsharingengineclassfactory_createinstance","mfsharingengine/IMFSharingEngineClassFactory::CreateInstance"]
old-location: mf\imfsharingengineclassfactory_createinstance.htm
tech.root: mf
ms.assetid: 8410FA9C-22C1-412D-90ED-55F19F21B8BD
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFSharingEngineClassFactory interface, IMFSharingEngineClassFactory interface [Media Foundation],CreateInstance method, IMFSharingEngineClassFactory.CreateInstance, IMFSharingEngineClassFactory::CreateInstance, mf.imfsharingengineclassfactory_createinstance, mfsharingengine/IMFSharingEngineClassFactory::CreateInstance
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
 - IMFSharingEngineClassFactory::CreateInstance
 - mfsharingengine/IMFSharingEngineClassFactory::CreateInstance
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
 - IMFSharingEngineClassFactory.CreateInstance
---

# IMFSharingEngineClassFactory::CreateInstance


## -description

Creates an instance of the media sharing engine.

## -parameters

### -param dwFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_createflags">MF_MEDIA_ENGINE_CREATEFLAGS</a> enumeration.

### -param pAttr [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. This parameter  specifies configuration attributes; see <a href="/windows/desktop/medfound/media-engine-attributes">Media Engine Attributes</a>.

### -param ppEngine [out]

Receives a pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the media sharing engine. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfsharingengineclassfactory">IMFSharingEngineClassFactory</a>
