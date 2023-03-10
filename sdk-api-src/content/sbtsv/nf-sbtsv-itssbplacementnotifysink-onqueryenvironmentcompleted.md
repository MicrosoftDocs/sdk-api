---
UID: NF:sbtsv.ITsSbPlacementNotifySink.OnQueryEnvironmentCompleted
title: ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the environment specified by the ITsSbClientConnection object is already hosting the correct target.
helpviewer_keywords: ["ITsSbPlacementNotifySink interface [Remote Desktop Services]","OnQueryEnvironmentCompleted method","ITsSbPlacementNotifySink.OnQueryEnvironmentCompleted","ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted","OnQueryEnvironmentCompleted","OnQueryEnvironmentCompleted method [Remote Desktop Services]","OnQueryEnvironmentCompleted method [Remote Desktop Services]","ITsSbPlacementNotifySink interface","sbtsv/ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted","termserv.itssbplacementnotifysink_onqueryenvironmentcompleted"]
old-location: termserv\itssbplacementnotifysink_onqueryenvironmentcompleted.htm
tech.root: TermServ
ms.assetid: 937982aa-7655-4681-ba6c-94201743c90c
ms.date: 12/05/2018
ms.keywords: ITsSbPlacementNotifySink interface [Remote Desktop Services],OnQueryEnvironmentCompleted method, ITsSbPlacementNotifySink.OnQueryEnvironmentCompleted, ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted, OnQueryEnvironmentCompleted, OnQueryEnvironmentCompleted method [Remote Desktop Services], OnQueryEnvironmentCompleted method [Remote Desktop Services],ITsSbPlacementNotifySink interface, sbtsv/ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted, termserv.itssbplacementnotifysink_onqueryenvironmentcompleted
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted
 - sbtsv/ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted
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
 - ITsSbPlacementNotifySink.OnQueryEnvironmentCompleted
---

# ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the environment 
specified by the <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a> object is already hosting the correct target.

## -parameters

### -param pEnvironment [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a> environment object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement">ITsSbPlacement</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink">ITsSbPlacementNotifySink</a>