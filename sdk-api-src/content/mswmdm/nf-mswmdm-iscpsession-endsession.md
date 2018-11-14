---
UID: NF:mswmdm.ISCPSession.EndSession
title: ISCPSession::EndSession
author: windows-sdk-content
description: The EndSession method indicates the ending of a transfer session.
old-location: wmdm\iscpsession_endsession.htm
tech.root: WMDM
ms.assetid: 322794ae-f8cd-4e2d-a329-728d281755cd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EndSession, EndSession method [windows Media Device Manager], EndSession method [windows Media Device Manager],ISCPSession interface, ISCPSession interface [windows Media Device Manager],EndSession method, ISCPSession.EndSession, ISCPSession::EndSession, ISCPSessionEndSession, mswmdm/ISCPSession::EndSession, wmdm.iscpsession_endsession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- ISCPSession.EndSession
: 
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

Pointer to an <a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a> object.


## -returns



If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4efd8e5a-490b-435b-b34d-7099198891b1">ISCPSession Interface</a>
 

 

