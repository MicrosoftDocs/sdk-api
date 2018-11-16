---
UID: NF:identitystore.IIdentityStore.GetCount
title: IIdentityStore::GetCount
author: windows-sdk-content
description: Gets the number of identity providers registered on the system.
old-location: security\iidentitystore_getcount.htm
tech.root: SecAuthN
ms.assetid: f7f30ab9-f55d-44fa-9098-c6bf865125f8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCount, GetCount method [Security], GetCount method [Security],IIdentityStore interface, IIdentityStore interface [Security],GetCount method, IIdentityStore.GetCount, IIdentityStore::GetCount, identitystore/IIdentityStore::GetCount, security.iidentitystore_getcount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: identitystore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identitystore.idl
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
 - Identitystore.h
api_name:
 - IIdentityStore.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- identitystore.h
: 
- IIdentityStore.GetCount
: 
---

# IIdentityStore::GetCount


## -description


The <b>GetCount</b> method gets the number of identity providers registered on the system.


## -parameters




### -param pdwProviders [out]

The number of identity providers registered on the system.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7f0f103-411b-4fbd-9ed5-30c6ab2f0ab6">IIdentityStore</a>
 

 

