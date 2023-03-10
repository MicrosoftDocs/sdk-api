---
UID: NF:wcmconfig.ISettingsContext.Serialize
title: ISettingsContext::Serialize (wcmconfig.h)
description: Serializes the data in this context into the provided stream.
helpviewer_keywords: ["ISettingsContext interface [SMI]","Serialize method","ISettingsContext.Serialize","ISettingsContext::Serialize","Serialize","Serialize method [SMI]","Serialize method [SMI]","ISettingsContext interface","smi.isettingscontext_serialize","wcmconfig/ISettingsContext::Serialize"]
old-location: smi\isettingscontext_serialize.htm
tech.root: SMI
ms.assetid: 13b29096-8572-4539-abd4-de22a9594f38
ms.date: 12/05/2018
ms.keywords: ISettingsContext interface [SMI],Serialize method, ISettingsContext.Serialize, ISettingsContext::Serialize, Serialize, Serialize method [SMI], Serialize method [SMI],ISettingsContext interface, smi.isettingscontext_serialize, wcmconfig/ISettingsContext::Serialize
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISettingsContext::Serialize
 - wcmconfig/ISettingsContext::Serialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsContext.Serialize
---

# ISettingsContext::Serialize


## -description

Serializes the data in this context into the provided stream.

## -parameters

### -param pStream [in]

The stream into which the XML, produced by the method, is inserted.

### -param pTarget [in]

Defines the parameters of the image against which the context must be serialized. This should match the target used while constructing the context.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingscontext">ISettingsContext</a>