---
UID: NF:identityprovider.IIdentityProvider.UnAdvise
title: IIdentityProvider::UnAdvise (identityprovider.h)
author: windows-sdk-content
description: Deletes a connection created by calling the Advise method.
old-location: security\iidentityprovider_unadvise.htm
tech.root: SecAuthN
ms.assetid: ba8a12fc-ea4c-45b5-8339-9cbc88c160db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIdentityProvider interface [Security],UnAdvise method, IIdentityProvider.UnAdvise, IIdentityProvider::UnAdvise, UnAdvise, UnAdvise method [Security], UnAdvise method [Security],IIdentityProvider interface, identityprovider/IIdentityProvider::UnAdvise, security.iidentityprovider_unadvise
ms.topic: method
f1_keywords: ["identityprovider/IIdentityProvider.UnAdvise"]
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
 - IIdentityProvider.UnAdvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdentityProvider::UnAdvise


## -description


The <b>UnAdvise</b> method deletes a connection created by calling the <a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">Advise</a> method.


## -parameters




### -param dwCookie [in]

A value that identifies the connection to delete.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">Advise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>
 

 

