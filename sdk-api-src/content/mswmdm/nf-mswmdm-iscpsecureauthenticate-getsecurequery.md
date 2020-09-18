---
UID: NF:mswmdm.ISCPSecureAuthenticate.GetSecureQuery
title: ISCPSecureAuthenticate::GetSecureQuery (mswmdm.h)
description: The GetSecureQuery method is used to obtain a pointer to the ISCPSecureQuery interface.
helpviewer_keywords: ["GetSecureQuery","GetSecureQuery method [windows Media Device Manager]","GetSecureQuery method [windows Media Device Manager]","ISCPSecureAuthenticate interface","ISCPSecureAuthenticate interface [windows Media Device Manager]","GetSecureQuery method","ISCPSecureAuthenticate.GetSecureQuery","ISCPSecureAuthenticate::GetSecureQuery","ISCPSecureAuthenticateGetSecureQuery","mswmdm/ISCPSecureAuthenticate::GetSecureQuery","wmdm.iscpsecureauthenticate_getsecurequery"]
old-location: wmdm\iscpsecureauthenticate_getsecurequery.htm
tech.root: WMDM
ms.assetid: d0cee36c-5200-4951-9a83-a0f32658939b
ms.date: 12/05/2018
ms.keywords: GetSecureQuery, GetSecureQuery method [windows Media Device Manager], GetSecureQuery method [windows Media Device Manager],ISCPSecureAuthenticate interface, ISCPSecureAuthenticate interface [windows Media Device Manager],GetSecureQuery method, ISCPSecureAuthenticate.GetSecureQuery, ISCPSecureAuthenticate::GetSecureQuery, ISCPSecureAuthenticateGetSecureQuery, mswmdm/ISCPSecureAuthenticate::GetSecureQuery, wmdm.iscpsecureauthenticate_getsecurequery
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISCPSecureAuthenticate::GetSecureQuery
 - mswmdm/ISCPSecureAuthenticate::GetSecureQuery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - ISCPSecureAuthenticate.GetSecureQuery
---

# ISCPSecureAuthenticate::GetSecureQuery


## -description

The <b>GetSecureQuery</b> method is used to obtain a pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery</a> interface.

## -parameters

### -param ppSecureQuery [out]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery</a> object.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate">ISCPSecureAuthenticate Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>