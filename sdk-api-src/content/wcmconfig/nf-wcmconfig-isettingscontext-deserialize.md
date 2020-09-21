---
UID: NF:wcmconfig.ISettingsContext.Deserialize
title: ISettingsContext::Deserialize (wcmconfig.h)
description: Deserializes the data in the stream that is provided to this context.
helpviewer_keywords: ["Deserialize","Deserialize method [SMI]","Deserialize method [SMI]","ISettingsContext interface","ISettingsContext interface [SMI]","Deserialize method","ISettingsContext.Deserialize","ISettingsContext::Deserialize","smi.isettingscontext_deserialize","wcmconfig/ISettingsContext::Deserialize"]
old-location: smi\isettingscontext_deserialize.htm
tech.root: SMI
ms.assetid: 382f2864-047e-4095-929b-a8b67773eefb
ms.date: 12/05/2018
ms.keywords: Deserialize, Deserialize method [SMI], Deserialize method [SMI],ISettingsContext interface, ISettingsContext interface [SMI],Deserialize method, ISettingsContext.Deserialize, ISettingsContext::Deserialize, smi.isettingscontext_deserialize, wcmconfig/ISettingsContext::Deserialize
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
 - ISettingsContext::Deserialize
 - wcmconfig/ISettingsContext::Deserialize
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
 - ISettingsContext.Deserialize
---

# ISettingsContext::Deserialize


## -description

Deserializes the data in the stream that is provided to this context.

## -parameters

### -param pStream [in]

A pointer to an IStream initialized stream object containing the XML representing a settings section of an answer (Unattend.xml) file.
An answers file is a file that facilitates the unattend process during setup or migration  to execute all of its tasks automatically, without user intervention.

### -param pTarget [in]

A pointer that identifies <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a> target object that should be used while deserializing the stream. This target should match the target which will be used on the engine alongside this context.

### -param pppResults [out]

A pointer to an array of <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsresult">ISettingsResult</a> interface pointers. Each interface pointer identifies an issue which may have occurred during deserialization.

### -param pcResultCount [out]

The number of ISettingsResult objects in the array pppResults.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_NAMESPACENOTFOUND</b> if pIdentity references a namespace that is not in the context.

This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources on the system to allocate the enumerators.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingscontext">ISettingsContext</a>