---
UID: NF:mfsharingengine.IPlayToSourceClassFactory.CreateInstance
title: IPlayToSourceClassFactory::CreateInstance (mfsharingengine.h)
description: Creates an instance of the PlayToController object.
helpviewer_keywords: ["CreateInstance","CreateInstance method [Media Foundation]","CreateInstance method [Media Foundation]","IPlayToSourceClassFactory interface","IPlayToSourceClassFactory interface [Media Foundation]","CreateInstance method","IPlayToSourceClassFactory.CreateInstance","IPlayToSourceClassFactory::CreateInstance","mf.iplaytocontrollerclassfactory_createinstance","mf.iplaytosourceclassfactory_createinstance","mfsharingengine/IPlayToSourceClassFactory::CreateInstance"]
old-location: mf\iplaytosourceclassfactory_createinstance.htm
tech.root: mf
ms.assetid: 3F7F8441-B0A2-407E-B127-C7DC66CA34DE
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IPlayToSourceClassFactory interface, IPlayToSourceClassFactory interface [Media Foundation],CreateInstance method, IPlayToSourceClassFactory.CreateInstance, IPlayToSourceClassFactory::CreateInstance, mf.iplaytocontrollerclassfactory_createinstance, mf.iplaytosourceclassfactory_createinstance, mfsharingengine/IPlayToSourceClassFactory::CreateInstance
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
 - IPlayToSourceClassFactory::CreateInstance
 - mfsharingengine/IPlayToSourceClassFactory::CreateInstance
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
 - IPlayToSourceClassFactory.CreateInstance
---

# IPlayToSourceClassFactory::CreateInstance


## -description

Creates an instance of the <b>PlayToController</b> object.

## -parameters

### -param dwFlags [in]

A bitwise <b>OR</b> of flags from the <a href="/windows/desktop/api/mfsharingengine/ne-mfsharingengine-playto_source_createflags">PLAYTO_SOURCE_CREATEFLAGS</a> enumeration.

### -param pControl [in]

A pointer to the <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrol">IPlayToControl</a> interface.

### -param ppSource [out]

Receives a pointer to the <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory">IPlayToSourceClassFactory</a>