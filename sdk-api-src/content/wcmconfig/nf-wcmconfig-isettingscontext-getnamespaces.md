---
UID: NF:wcmconfig.ISettingsContext.GetNamespaces
title: ISettingsContext::GetNamespaces (wcmconfig.h)
description: Gets the namespaces that exist in the context.
helpviewer_keywords: ["GetNamespaces","GetNamespaces method [SMI]","GetNamespaces method [SMI]","ISettingsContext interface","ISettingsContext interface [SMI]","GetNamespaces method","ISettingsContext.GetNamespaces","ISettingsContext::GetNamespaces","smi.isettingscontext_getnamespaces","wcmconfig/ISettingsContext::GetNamespaces"]
old-location: smi\isettingscontext_getnamespaces.htm
tech.root: SMI
ms.assetid: 844ef731-9ccf-4cf5-9bb9-218312cbb07c
ms.date: 12/05/2018
ms.keywords: GetNamespaces, GetNamespaces method [SMI], GetNamespaces method [SMI],ISettingsContext interface, ISettingsContext interface [SMI],GetNamespaces method, ISettingsContext.GetNamespaces, ISettingsContext::GetNamespaces, smi.isettingscontext_getnamespaces, wcmconfig/ISettingsContext::GetNamespaces
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
 - ISettingsContext::GetNamespaces
 - wcmconfig/ISettingsContext::GetNamespaces
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
 - ISettingsContext.GetNamespaces
---

# ISettingsContext::GetNamespaces


## -description

Gets the namespaces that exist in the context.

## -parameters

### -param ppNamespaceIds [out]

An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a> interface pointer that represents the collection of namespaces.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -remarks

<div class="alert"><b>Note</b>  This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources in the system to allocate a new enumerator.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingscontext">ISettingsContext</a>