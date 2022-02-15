---
UID: NF:sbtsv.ITsSbGenericNotifySink.OnCompleted
title: ITsSbGenericNotifySink::OnCompleted (sbtsv.h)
description: Reports completion to Remote Desktop Connection Broker (RD Connection Broker).
helpviewer_keywords: ["ITsSbGenericNotifySink interface [Remote Desktop Services]","OnCompleted method","ITsSbGenericNotifySink.OnCompleted","ITsSbGenericNotifySink::OnCompleted","OnCompleted","OnCompleted method [Remote Desktop Services]","OnCompleted method [Remote Desktop Services]","ITsSbGenericNotifySink interface","sbtsv/ITsSbGenericNotifySink::OnCompleted","termserv.itssbgenericnotifysink_oncompleted"]
old-location: termserv\itssbgenericnotifysink_oncompleted.htm
tech.root: TermServ
ms.assetid: 6d8dd044-988e-4e37-9936-2a3639dedca1
ms.date: 12/05/2018
ms.keywords: ITsSbGenericNotifySink interface [Remote Desktop Services],OnCompleted method, ITsSbGenericNotifySink.OnCompleted, ITsSbGenericNotifySink::OnCompleted, OnCompleted, OnCompleted method [Remote Desktop Services], OnCompleted method [Remote Desktop Services],ITsSbGenericNotifySink interface, sbtsv/ITsSbGenericNotifySink::OnCompleted, termserv.itssbgenericnotifysink_oncompleted
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SbTsV.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbGenericNotifySink::OnCompleted
 - sbtsv/ITsSbGenericNotifySink::OnCompleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbGenericNotifySink.OnCompleted
---

# ITsSbGenericNotifySink::OnCompleted


## -description

Reports completion to Remote Desktop Connection Broker (RD Connection Broker).

## -parameters

### -param Status [in]

The status to report.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink">ITsSbGenericNotifySink</a>