---
UID: NF:identityprovider.IIdentityProvider.Import
title: IIdentityProvider::Import
author: windows-sdk-content
description: Imports an identity to the system.
old-location: security\iidentityprovider_import.htm
tech.root: secauthn
ms.assetid: 16cf4e84-1a68-4794-a456-1a9f5ce4896d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIdentityProvider interface [Security],Import method, IIdentityProvider.Import, IIdentityProvider::Import, Import, Import method [Security], Import method [Security],IIdentityProvider interface, identityprovider/IIdentityProvider::Import, security.iidentityprovider_import
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
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
 - Identityprovider.h
api_name:
 - IIdentityProvider.Import
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityProvider::Import


## -description


The <b>Import</b> method imports an identity to the system.


## -parameters




### -param pPropertyStore [in]

A pointer to the <b>IPropertyStore</b> interface that specifies all information required to create the new identity on the system.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

