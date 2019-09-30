---
UID: NF:mswmdm.ISCPSession.EndSession
title: ISCPSession::EndSession (mswmdm.h)
author: windows-sdk-content
description: The EndSession method indicates the ending of a transfer session.
old-location: wmdm\iscpsession_endsession.htm
tech.root: WMDM
ms.assetid: 322794ae-f8cd-4e2d-a329-728d281755cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndSession, EndSession method [windows Media Device Manager], EndSession method [windows Media Device Manager],ISCPSession interface, ISCPSession interface [windows Media Device Manager],EndSession method, ISCPSession.EndSession, ISCPSession::EndSession, ISCPSessionEndSession, mswmdm/ISCPSession::EndSession, wmdm.iscpsession_endsession
ms.topic: method
f1_keywords: 
 - "mswmdm/ISCPSession.EndSession"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCPSession::EndSession


## -description



The <b>EndSession</b> method indicates the ending of a transfer session.




## -parameters




### -param pCtx [in]

Pointer to the context.


### -param dwSizeCtx [in]

<b>DWORD</b> containing the size of context.


#### - pIDevice [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> object.


## -returns



If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession">ISCPSession Interface</a>
 

 

