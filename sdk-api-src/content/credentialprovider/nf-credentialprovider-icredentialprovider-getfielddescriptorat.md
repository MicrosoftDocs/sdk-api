---
UID: NF:credentialprovider.ICredentialProvider.GetFieldDescriptorAt
title: ICredentialProvider::GetFieldDescriptorAt
author: windows-sdk-content
description: Gets metadata that describes a specified field.
old-location: shell\ICredentialProvider_GetFieldDescriptorAt.htm
tech.root: shell
ms.assetid: bb9f063d-afbc-4f6b-a4a5-19a9a644f029
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetFieldDescriptorAt, GetFieldDescriptorAt method [Windows Shell], GetFieldDescriptorAt method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetFieldDescriptorAt method, ICredentialProvider.GetFieldDescriptorAt, ICredentialProvider::GetFieldDescriptorAt, credentialprovider/ICredentialProvider::GetFieldDescriptorAt, shell.ICredentialProvider_GetFieldDescriptorAt, shell_ICredentialProvider_GetFieldDescriptorAt
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
 - ICredentialProvider.GetFieldDescriptorAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProvider::GetFieldDescriptorAt


## -description


Gets metadata that describes a specified field.


## -parameters




### -param dwIndex [in]

Type: <b>DWORD</b>

The zero-based index of the field for which the information should be retrieved.


### -param ppcpfd [out]

Type: <b><a href="https://msdn.microsoft.com/8409b4b7-c601-4e85-95f9-4272feb29028">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a>**</b>

The address of a pointer to a <a href="https://msdn.microsoft.com/8409b4b7-c601-4e85-95f9-4272feb29028">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> structure which receives the information about the field.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is required.





