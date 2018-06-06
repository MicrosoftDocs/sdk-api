---
UID: NF:mswmdm.ISCPSession.BeginSession
title: ISCPSession::BeginSession
author: windows-sdk-content
description: The BeginSession method indicates beginning of a transfer session. It can be used to optimize operations that need to occur only once per transfer session.
old-location: wmdm\iscpsession_beginsession.htm
old-project: WMDM
ms.assetid: da458458-5828-4ab4-8793-d59a07f46569
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: BeginSession, BeginSession method [windows Media Device Manager], BeginSession method [windows Media Device Manager],ISCPSession interface, ISCPSession interface [windows Media Device Manager],BeginSession method, ISCPSession.BeginSession, ISCPSession::BeginSession, ISCPSessionBeginSession, mswmdm/ISCPSession::BeginSession, wmdm.iscpsession_beginsession
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
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
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISCPSession::BeginSession


## -description



The <b>BeginSession</b> method indicates beginning of a transfer session. It can be used to optimize operations that need to occur only once per transfer session.




## -parameters




### -param pIDevice [in]

Pointer to an <a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a> object.


### -param pCtx [in]

Pointer to the context.


### -param dwSizeCtx [in]

<b>DWORD</b> containing the size of context.


## -returns



If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4efd8e5a-490b-435b-b34d-7099198891b1">ISCPSession Interface</a>
 

 

