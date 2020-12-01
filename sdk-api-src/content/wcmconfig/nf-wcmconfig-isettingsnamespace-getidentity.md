---
UID: NF:wcmconfig.ISettingsNamespace.GetIdentity
title: ISettingsNamespace::GetIdentity (wcmconfig.h)
description: Gets the identity of the namespace.
helpviewer_keywords: ["GetIdentity","GetIdentity method [SMI]","GetIdentity method [SMI]","ISettingsNamespace interface","ISettingsNamespace interface [SMI]","GetIdentity method","ISettingsNamespace.GetIdentity","ISettingsNamespace::GetIdentity","smi.isettingsnamespace_getidentity","wcmconfig/ISettingsNamespace::GetIdentity"]
old-location: smi\isettingsnamespace_getidentity.htm
tech.root: SMI
ms.assetid: a61c629f-4f7b-46f8-bdeb-543523bc2bea
ms.date: 12/05/2018
ms.keywords: GetIdentity, GetIdentity method [SMI], GetIdentity method [SMI],ISettingsNamespace interface, ISettingsNamespace interface [SMI],GetIdentity method, ISettingsNamespace.GetIdentity, ISettingsNamespace::GetIdentity, smi.isettingsnamespace_getidentity, wcmconfig/ISettingsNamespace::GetIdentity
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
 - ISettingsNamespace::GetIdentity
 - wcmconfig/ISettingsNamespace::GetIdentity
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
 - ISettingsNamespace.GetIdentity
---

# ISettingsNamespace::GetIdentity


## -description

Gets the identity of the namespace.

## -parameters

### -param SettingsID [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsidentity">ISettingsIdentity</a> object that represents the namespace identity.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsnamespace">ISettingsNamespace</a>