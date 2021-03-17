---
UID: NF:mswmdm.ISCPSession.EndSession
title: ISCPSession::EndSession (mswmdm.h)
description: The EndSession method indicates the ending of a transfer session.
helpviewer_keywords: ["EndSession","EndSession method [windows Media Device Manager]","EndSession method [windows Media Device Manager]","ISCPSession interface","ISCPSession interface [windows Media Device Manager]","EndSession method","ISCPSession.EndSession","ISCPSession::EndSession","ISCPSessionEndSession","mswmdm/ISCPSession::EndSession","wmdm.iscpsession_endsession"]
old-location: wmdm\iscpsession_endsession.htm
tech.root: WMDM
ms.assetid: 322794ae-f8cd-4e2d-a329-728d281755cd
ms.date: 12/05/2018
ms.keywords: EndSession, EndSession method [windows Media Device Manager], EndSession method [windows Media Device Manager],ISCPSession interface, ISCPSession interface [windows Media Device Manager],EndSession method, ISCPSession.EndSession, ISCPSession::EndSession, ISCPSessionEndSession, mswmdm/ISCPSession::EndSession, wmdm.iscpsession_endsession
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
 - ISCPSession::EndSession
 - mswmdm/ISCPSession::EndSession
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
 - ISCPSession.EndSession
---

# ISCPSession::EndSession


## -description

The <b>EndSession</b> method indicates the ending of a transfer session.

## -parameters

### -param pCtx [in]

Pointer to the context.

### -param dwSizeCtx [in]

<b>DWORD</b> containing the size of context.


## -returns

If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession">ISCPSession Interface</a>