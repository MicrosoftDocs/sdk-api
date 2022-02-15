---
UID: NF:credentialprovider.ICredentialProvider.GetFieldDescriptorCount
title: ICredentialProvider::GetFieldDescriptorCount (credentialprovider.h)
description: Retrieves the count of fields in the needed to display this provider's credentials.
helpviewer_keywords: ["GetFieldDescriptorCount","GetFieldDescriptorCount method [Windows Shell]","GetFieldDescriptorCount method [Windows Shell]","ICredentialProvider interface","ICredentialProvider interface [Windows Shell]","GetFieldDescriptorCount method","ICredentialProvider.GetFieldDescriptorCount","ICredentialProvider::GetFieldDescriptorCount","credentialprovider/ICredentialProvider::GetFieldDescriptorCount","shell.ICredentialProvider_GetFieldDescriptorCount","shell_ICredentialProvider_GetFieldDescriptorCount"]
old-location: shell\ICredentialProvider_GetFieldDescriptorCount.htm
tech.root: shell
ms.assetid: dacaa846-1838-4348-ba63-c204cbe0e2ae
ms.date: 12/05/2018
ms.keywords: GetFieldDescriptorCount, GetFieldDescriptorCount method [Windows Shell], GetFieldDescriptorCount method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetFieldDescriptorCount method, ICredentialProvider.GetFieldDescriptorCount, ICredentialProvider::GetFieldDescriptorCount, credentialprovider/ICredentialProvider::GetFieldDescriptorCount, shell.ICredentialProvider_GetFieldDescriptorCount, shell_ICredentialProvider_GetFieldDescriptorCount
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
 - ICredentialProvider::GetFieldDescriptorCount
 - credentialprovider/ICredentialProvider::GetFieldDescriptorCount
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
 - ICredentialProvider.GetFieldDescriptorCount
---

# ICredentialProvider::GetFieldDescriptorCount


## -description

Retrieves the count of fields in the needed to display this provider's credentials.

## -parameters

### -param pdwCount [out]

Type: <b>DWORD*</b>

Pointer to the field count.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is required.

The count provided by this method must be valid for the entire usage scenario. This means that you need to include all fields, even those that are hidden or only shown under special circumstances. This value cannot be changed during a usage scenario and can only be changed when a new <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setusagescenario">SetUsageScenario</a> call is made to the provider or the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialproviderevents">ICredentialProviderEvents</a> instance forces another enumeration.