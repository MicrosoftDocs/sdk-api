---
UID: NF:mswmdm.ISCPSecureAuthenticate2.GetSCPSession
title: ISCPSecureAuthenticate2::GetSCPSession (mswmdm.h)
description: The GetSCPSession method is used to obtain a pointer to the ISCPSecureQuery interface that represents a session object.
helpviewer_keywords: ["GetSCPSession","GetSCPSession method [windows Media Device Manager]","GetSCPSession method [windows Media Device Manager]","ISCPSecureAuthenticate2 interface","ISCPSecureAuthenticate2 interface [windows Media Device Manager]","GetSCPSession method","ISCPSecureAuthenticate2.GetSCPSession","ISCPSecureAuthenticate2::GetSCPSession","ISCPSecureAuthenticate2GetSCPSession","mswmdm/ISCPSecureAuthenticate2::GetSCPSession","wmdm.iscpsecureauthenticate2_getscpsession"]
old-location: wmdm\iscpsecureauthenticate2_getscpsession.htm
tech.root: WMDM
ms.assetid: 7e09d8ea-65aa-427b-a876-00b089659b1b
ms.date: 12/05/2018
ms.keywords: GetSCPSession, GetSCPSession method [windows Media Device Manager], GetSCPSession method [windows Media Device Manager],ISCPSecureAuthenticate2 interface, ISCPSecureAuthenticate2 interface [windows Media Device Manager],GetSCPSession method, ISCPSecureAuthenticate2.GetSCPSession, ISCPSecureAuthenticate2::GetSCPSession, ISCPSecureAuthenticate2GetSCPSession, mswmdm/ISCPSecureAuthenticate2::GetSCPSession, wmdm.iscpsecureauthenticate2_getscpsession
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
 - ISCPSecureAuthenticate2::GetSCPSession
 - mswmdm/ISCPSecureAuthenticate2::GetSCPSession
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
 - ISCPSecureAuthenticate2.GetSCPSession
---

# ISCPSecureAuthenticate2::GetSCPSession


## -description

The <b>GetSCPSession</b> method is used to obtain a pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery</a> interface that represents a session object.

## -parameters

### -param ppSCPSession [out]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession">ISCPSession</a> object.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used to obtain a secure content provider (SCP) session. An SCP session is useful during transfer of multiple files, where the session can help SCP do some of the operations only once instead of once for every file transfer. This results in better transfer performance.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2">ISCPSecureAuthenticate2 Interface</a>