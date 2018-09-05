---
UID: NF:identityprovider.IIdentityProvider.UnAdvise
title: IIdentityProvider::UnAdvise
author: windows-sdk-content
description: Deletes a connection created by calling the Advise method.
old-location: security\iidentityprovider_unadvise.htm
old-project: SecAuthN
ms.assetid: ba8a12fc-ea4c-45b5-8339-9cbc88c160db
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IIdentityProvider interface [Security],UnAdvise method, IIdentityProvider.UnAdvise, IIdentityProvider::UnAdvise, UnAdvise, UnAdvise method [Security], UnAdvise method [Security],IIdentityProvider interface, identityprovider/IIdentityProvider::UnAdvise, security.iidentityprovider_unadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: identityprovider.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: IDENTITY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IIdentityProvider.UnAdvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIdentityProvider::UnAdvise


## -description


The <b>UnAdvise</b> method deletes a connection created by calling the <a href="https://msdn.microsoft.com/fcac9d30-64ed-4746-aacc-ee659c2b2642">Advise</a> method.


## -parameters




### -param dwCookie [in]

A value that identifies the connection to delete.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/fcac9d30-64ed-4746-aacc-ee659c2b2642">Advise</a>



<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

