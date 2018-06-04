---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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





