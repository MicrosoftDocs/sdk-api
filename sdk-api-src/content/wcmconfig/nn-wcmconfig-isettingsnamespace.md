---
UID: NN:wcmconfig.ISettingsNamespace
title: ISettingsNamespace (wcmconfig.h)
description: Performs operations to set, retrieve, and validate settings, and save changes for a namespace instance.
helpviewer_keywords: ["ISettingsNamespace","ISettingsNamespace interface [SMI]","ISettingsNamespace interface [SMI]","described","smi.isettingsnamespace","wcmconfig/ISettingsNamespace"]
old-location: smi\isettingsnamespace.htm
tech.root: SMI
ms.assetid: a5d7b9ff-eb6f-40be-b246-17189cad92be
ms.date: 12/05/2018
ms.keywords: ISettingsNamespace, ISettingsNamespace interface [SMI], ISettingsNamespace interface [SMI],described, smi.isettingsnamespace, wcmconfig/ISettingsNamespace
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
 - ISettingsNamespace
 - wcmconfig/ISettingsNamespace
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
 - ISettingsNamespace
---

# ISettingsNamespace interface


## -description

Performs operations to set, retrieve, and validate settings, and save changes for a namespace instance.

To retrieve an <b>ISettingsNamespace</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-getnamespace">ISettingsEngine::GetNamespace</a> method.

## -inheritance

The <b>ISettingsNamespace</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISettingsNamespace</b> also has these types of members:

