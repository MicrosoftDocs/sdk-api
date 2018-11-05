---
UID: NF:credentialprovider.ICredentialProvider.GetFieldDescriptorCount
title: ICredentialProvider::GetFieldDescriptorCount
author: windows-sdk-content
description: Retrieves the count of fields in the needed to display this provider's credentials.
old-location: shell\ICredentialProvider_GetFieldDescriptorCount.htm
tech.root: shell
ms.assetid: dacaa846-1838-4348-ba63-c204cbe0e2ae
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetFieldDescriptorCount, GetFieldDescriptorCount method [Windows Shell], GetFieldDescriptorCount method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetFieldDescriptorCount method, ICredentialProvider.GetFieldDescriptorCount, ICredentialProvider::GetFieldDescriptorCount, credentialprovider/ICredentialProvider::GetFieldDescriptorCount, shell.ICredentialProvider_GetFieldDescriptorCount, shell_ICredentialProvider_GetFieldDescriptorCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProvider.GetFieldDescriptorCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required.

The count provided by this method must be valid for the entire usage scenario. This means that you need to include all fields, even those that are hidden or only shown under special circumstances. This value cannot be changed during a usage scenario and can only be changed when a new <a href="https://msdn.microsoft.com/62577b41-e115-45df-9f9b-c5c282365a3e">SetUsageScenario</a> call is made to the provider or the <a href="https://msdn.microsoft.com/bf303b9d-2d6c-4de5-9bca-fc71d4f18903">ICredentialProviderEvents</a> instance forces another enumeration.



