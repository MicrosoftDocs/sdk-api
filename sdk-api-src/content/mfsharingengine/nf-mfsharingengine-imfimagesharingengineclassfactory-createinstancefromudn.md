---
UID: NF:mfsharingengine.IMFImageSharingEngineClassFactory.CreateInstanceFromUDN
title: IMFImageSharingEngineClassFactory::CreateInstanceFromUDN (mfsharingengine.h)
description: Creates an instance of the IMFImageSharingEngine from the provided unique device name.
helpviewer_keywords: ["CreateInstanceFromUDN","CreateInstanceFromUDN method [Media Foundation]","CreateInstanceFromUDN method [Media Foundation]","IMFImageSharingEngineClassFactory interface","IMFImageSharingEngineClassFactory interface [Media Foundation]","CreateInstanceFromUDN method","IMFImageSharingEngineClassFactory.CreateInstanceFromUDN","IMFImageSharingEngineClassFactory::CreateInstanceFromUDN","mf.imfimagesharingengineclassfactory_createinstancefromudn","mfsharingengine/IMFImageSharingEngineClassFactory::CreateInstanceFromUDN"]
old-location: mf\imfimagesharingengineclassfactory_createinstancefromudn.htm
tech.root: mf
ms.assetid: 343E9CB5-12CA-4AC9-857F-D8324D035F07
ms.date: 12/05/2018
ms.keywords: CreateInstanceFromUDN, CreateInstanceFromUDN method [Media Foundation], CreateInstanceFromUDN method [Media Foundation],IMFImageSharingEngineClassFactory interface, IMFImageSharingEngineClassFactory interface [Media Foundation],CreateInstanceFromUDN method, IMFImageSharingEngineClassFactory.CreateInstanceFromUDN, IMFImageSharingEngineClassFactory::CreateInstanceFromUDN, mf.imfimagesharingengineclassfactory_createinstancefromudn, mfsharingengine/IMFImageSharingEngineClassFactory::CreateInstanceFromUDN
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
 - IMFImageSharingEngineClassFactory::CreateInstanceFromUDN
 - mfsharingengine/IMFImageSharingEngineClassFactory::CreateInstanceFromUDN
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
 - IMFImageSharingEngineClassFactory.CreateInstanceFromUDN
---

# IMFImageSharingEngineClassFactory::CreateInstanceFromUDN


## -description

Creates an instance of the <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine">IMFImageSharingEngine</a> from the provided unique device name.

## -parameters

### -param pUniqueDeviceName

The unique device name of the device with which the sharing engine is created.

### -param ppEngine [out]

Receives a pointer to the <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine">IMFImageSharingEngine</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengineclassfactory">IMFImageSharingEngineClassFactory</a>