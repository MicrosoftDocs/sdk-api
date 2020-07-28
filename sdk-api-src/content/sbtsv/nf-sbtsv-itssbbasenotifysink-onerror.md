---
UID: NF:sbtsv.ITsSbBaseNotifySink.OnError
title: ITsSbBaseNotifySink::OnError (sbtsv.h)
description: Reports an error condition to Remote Desktop Connection Broker (RD Connection Broker).
helpviewer_keywords: ["ITsSbBaseNotifySink interface [Remote Desktop Services]","OnError method","ITsSbBaseNotifySink.OnError","ITsSbBaseNotifySink::OnError","OnError","OnError method [Remote Desktop Services]","OnError method [Remote Desktop Services]","ITsSbBaseNotifySink interface","sbtsv/ITsSbBaseNotifySink::OnError","termserv.itssbbasenotifysink_onerror"]
old-location: termserv\itssbbasenotifysink_onerror.htm
tech.root: TermServ
ms.assetid: d8101644-51b4-45a8-8696-7dbb28aaaf0b
ms.date: 12/05/2018
ms.keywords: ITsSbBaseNotifySink interface [Remote Desktop Services],OnError method, ITsSbBaseNotifySink.OnError, ITsSbBaseNotifySink::OnError, OnError, OnError method [Remote Desktop Services], OnError method [Remote Desktop Services],ITsSbBaseNotifySink interface, sbtsv/ITsSbBaseNotifySink::OnError, termserv.itssbbasenotifysink_onerror
f1_keywords:
- sbtsv/ITsSbBaseNotifySink.OnError
dev_langs:
- c++
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
- sbtsv.h
api_name:
- ITsSbBaseNotifySink.OnError
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbBaseNotifySink::OnError


## -description


Reports an error condition to Remote Desktop Connection Broker (RD Connection Broker).


## -parameters




### -param hrError [in]

The error condition.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this  method stops further processing on the client connection and causes the connection to fail.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>
 

 

