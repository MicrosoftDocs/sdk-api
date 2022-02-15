---
UID: NN:credentialprovider.ICredentialProviderFilter
title: ICredentialProviderFilter (credentialprovider.h)
description: Used to dynamically filter credential providers based on information available at runtime.
helpviewer_keywords: ["ICredentialProviderFilter","ICredentialProviderFilter interface [Windows Shell]","ICredentialProviderFilter interface [Windows Shell]","described","_shell_ICredentialProviderFilter","credentialprovider/ICredentialProviderFilter","shell.ICredentialProviderFilter"]
old-location: shell\ICredentialProviderFilter.htm
tech.root: shell
ms.assetid: a12a0648-ea60-4537-9d5c-8d21fd53cc80
ms.date: 12/05/2018
ms.keywords: ICredentialProviderFilter, ICredentialProviderFilter interface [Windows Shell], ICredentialProviderFilter interface [Windows Shell],described, _shell_ICredentialProviderFilter, credentialprovider/ICredentialProviderFilter, shell.ICredentialProviderFilter
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
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
 - ICredentialProviderFilter
 - credentialprovider/ICredentialProviderFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProviderFilter
---

# ICredentialProviderFilter interface


## -description

Used to dynamically filter credential providers based on information available at runtime.

## -inheritance

The <b>ICredentialProviderFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderFilter</b> also has these types of members:

## -remarks

It is recommended that third party credential providers do not use this interface to filter or disable system credential providers on a desktop. If an enterprise deploys a third party credential provider and wants to disable system credential providers currently available, that is a decision that should be made by a domain administrator after careful consideration. System policies exist that enable administrators to filter out credential providers and those should be used instead of building filters directly into a third party credential provider.
