---
UID: NF:mswmdm.ISCPSession.GetSecureQuery
title: ISCPSession::GetSecureQuery (mswmdm.h)
description: The GetSecureQuery method is used to obtain a secure query object for the session.
helpviewer_keywords: ["GetSecureQuery","GetSecureQuery method [windows Media Device Manager]","GetSecureQuery method [windows Media Device Manager]","ISCPSession interface","ISCPSession interface [windows Media Device Manager]","GetSecureQuery method","ISCPSession.GetSecureQuery","ISCPSession::GetSecureQuery","ISCPSessionGetSecureQuerry","mswmdm/ISCPSession::GetSecureQuery","wmdm.iscpsession_getsecurequery"]
old-location: wmdm\iscpsession_getsecurequery.htm
tech.root: WMDM
ms.assetid: c725f0ae-1f37-412d-ac2b-0833989d1bd6
ms.date: 12/05/2018
ms.keywords: GetSecureQuery, GetSecureQuery method [windows Media Device Manager], GetSecureQuery method [windows Media Device Manager],ISCPSession interface, ISCPSession interface [windows Media Device Manager],GetSecureQuery method, ISCPSession.GetSecureQuery, ISCPSession::GetSecureQuery, ISCPSessionGetSecureQuerry, mswmdm/ISCPSession::GetSecureQuery, wmdm.iscpsession_getsecurequery
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
 - ISCPSession::GetSecureQuery
 - mswmdm/ISCPSession::GetSecureQuery
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
 - ISCPSession.GetSecureQuery
---

# ISCPSession::GetSecureQuery


## -description

The <b>GetSecureQuery</b> method is used to obtain a secure query object for the session.

## -parameters

### -param ppSecureQuery [out]

Pointer to a secure query object.

## -returns

If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method should be used to obtain a secure query object when using secure content provider sessions for efficient transfer of multiple files.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession">ISCPSession Interface</a>