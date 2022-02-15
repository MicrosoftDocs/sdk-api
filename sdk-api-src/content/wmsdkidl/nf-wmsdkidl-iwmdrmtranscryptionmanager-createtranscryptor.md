---
UID: NF:wmsdkidl.IWMDRMTranscryptionManager.CreateTranscryptor
title: IWMDRMTranscryptionManager::CreateTranscryptor (wmsdkidl.h)
description: Creates a DRM transcryptor object.
helpviewer_keywords: ["CreateTranscryptor","CreateTranscryptor method [windows Media Format]","CreateTranscryptor method [windows Media Format]","IWMDRMTranscryptionManager interface","IWMDRMTranscryptionManager interface [windows Media Format]","CreateTranscryptor method","IWMDRMTranscryptionManager.CreateTranscryptor","IWMDRMTranscryptionManager::CreateTranscryptor","wmformat.iwmdrmtranscryptionmanager_createtranscryptor","wmsdkidl/IWMDRMTranscryptionManager::CreateTranscryptor"]
old-location: wmformat\iwmdrmtranscryptionmanager_createtranscryptor.htm
tech.root: wmformat
ms.assetid: e4dfa908-9fd2-4968-b4a0-c7b69064d46e
ms.date: 12/05/2018
ms.keywords: CreateTranscryptor, CreateTranscryptor method [windows Media Format], CreateTranscryptor method [windows Media Format],IWMDRMTranscryptionManager interface, IWMDRMTranscryptionManager interface [windows Media Format],CreateTranscryptor method, IWMDRMTranscryptionManager.CreateTranscryptor, IWMDRMTranscryptionManager::CreateTranscryptor, wmformat.iwmdrmtranscryptionmanager_createtranscryptor, wmsdkidl/IWMDRMTranscryptionManager::CreateTranscryptor
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IWMDRMTranscryptionManager::CreateTranscryptor
 - wmsdkidl/IWMDRMTranscryptionManager::CreateTranscryptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMDRMTranscryptionManager.CreateTranscryptor
---

# IWMDRMTranscryptionManager::CreateTranscryptor


## -description

Creates a DRM transcryptor object.

## -parameters

### -param ppTranscryptor [out]

Address of a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor">IWMDRMTranscryptor</a> interface of the newly created DRM transcryptor object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd798365(v=vs.85)">IWMDRMTranscryptionManager</a>