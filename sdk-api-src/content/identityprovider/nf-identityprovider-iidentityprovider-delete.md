---
UID: NF:identityprovider.IIdentityProvider.Delete
title: IIdentityProvider::Delete
author: windows-sdk-content
description: Removes the specified identity from the identity store or the specified properties from the identity.
old-location: security\iidentityprovider_delete.htm
tech.root: SecAuthN
ms.assetid: a21aa2eb-2551-4920-a312-34fa327572ca
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Delete, Delete method [Security], Delete method [Security],IIdentityProvider interface, IIdentityProvider interface [Security],Delete method, IIdentityProvider.Delete, IIdentityProvider::Delete, identityprovider/IIdentityProvider::Delete, security.iidentityprovider_delete
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
 - IIdentityProvider.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityProvider::Delete


## -description


The <b>Delete</b> method removes the specified identity from the identity store or the specified properties from the identity.


## -parameters




### -param lpszUniqueID [in]

The unique name associated with the identity.


### -param pKeywordsToDelete [in, optional]

The names of properties to delete. If the value of this parameter is <b>NULL</b>, the identity is deleted.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

