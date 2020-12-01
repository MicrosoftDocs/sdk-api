---
UID: NF:mswmdm.ISCPSession.BeginSession
title: ISCPSession::BeginSession (mswmdm.h)
description: The BeginSession method indicates beginning of a transfer session. It can be used to optimize operations that need to occur only once per transfer session.
helpviewer_keywords: ["BeginSession","BeginSession method [windows Media Device Manager]","BeginSession method [windows Media Device Manager]","ISCPSession interface","ISCPSession interface [windows Media Device Manager]","BeginSession method","ISCPSession.BeginSession","ISCPSession::BeginSession","ISCPSessionBeginSession","mswmdm/ISCPSession::BeginSession","wmdm.iscpsession_beginsession"]
old-location: wmdm\iscpsession_beginsession.htm
tech.root: WMDM
ms.assetid: da458458-5828-4ab4-8793-d59a07f46569
ms.date: 12/05/2018
ms.keywords: BeginSession, BeginSession method [windows Media Device Manager], BeginSession method [windows Media Device Manager],ISCPSession interface, ISCPSession interface [windows Media Device Manager],BeginSession method, ISCPSession.BeginSession, ISCPSession::BeginSession, ISCPSessionBeginSession, mswmdm/ISCPSession::BeginSession, wmdm.iscpsession_beginsession
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
 - ISCPSession::BeginSession
 - mswmdm/ISCPSession::BeginSession
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
 - ISCPSession.BeginSession
---

# ISCPSession::BeginSession


## -description

The <b>BeginSession</b> method indicates beginning of a transfer session. It can be used to optimize operations that need to occur only once per transfer session.

## -parameters

### -param pIDevice [in]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> object.

### -param pCtx [in]

Pointer to the context.

### -param dwSizeCtx [in]

<b>DWORD</b> containing the size of context.

## -returns

If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession">ISCPSession Interface</a>