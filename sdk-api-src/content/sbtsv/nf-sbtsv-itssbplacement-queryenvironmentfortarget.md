---
UID: NF:sbtsv.ITsSbPlacement.QueryEnvironmentForTarget
title: ITsSbPlacement::QueryEnvironmentForTarget (sbtsv.h)
description: Determines whether the specified environment is ready to host the target that was returned by load balancing.
helpviewer_keywords: ["ITsSbPlacement interface [Remote Desktop Services]","QueryEnvironmentForTarget method","ITsSbPlacement.QueryEnvironmentForTarget","ITsSbPlacement::QueryEnvironmentForTarget","QueryEnvironmentForTarget","QueryEnvironmentForTarget method [Remote Desktop Services]","QueryEnvironmentForTarget method [Remote Desktop Services]","ITsSbPlacement interface","sbtsv/ITsSbPlacement::QueryEnvironmentForTarget","termserv.itssbplacement_queryenvironmentfortarget"]
old-location: termserv\itssbplacement_queryenvironmentfortarget.htm
tech.root: TermServ
ms.assetid: 62320a0b-3f3e-4341-a481-a43af39c06f7
ms.date: 12/05/2018
ms.keywords: ITsSbPlacement interface [Remote Desktop Services],QueryEnvironmentForTarget method, ITsSbPlacement.QueryEnvironmentForTarget, ITsSbPlacement::QueryEnvironmentForTarget, QueryEnvironmentForTarget, QueryEnvironmentForTarget method [Remote Desktop Services], QueryEnvironmentForTarget method [Remote Desktop Services],ITsSbPlacement interface, sbtsv/ITsSbPlacement::QueryEnvironmentForTarget, termserv.itssbplacement_queryenvironmentfortarget
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
 - ITsSbPlacement::QueryEnvironmentForTarget
 - sbtsv/ITsSbPlacement::QueryEnvironmentForTarget
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
 - ITsSbPlacement.QueryEnvironmentForTarget
---

# ITsSbPlacement::QueryEnvironmentForTarget


## -description

Determines whether the specified environment is ready to host 
the target that was returned by load balancing.

## -parameters

### -param pConnection [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a> client connection object.

### -param pPlacementSink [in]

 A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink">ITsSbPlacementNotifySink</a> placement sink object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Your plug-in should use the <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink">ITsSbPlacementNotifySink</a> object to report the state of the environment to Remote Desktop Connection Broker (RD Connection Broker).

After RD Connection Broker receives a load-balancing result, it calls <b>QueryEnvironmentForTarget</b> 
to determine whether the environment is present and ready.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement">ITsSbPlacement</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink">ITsSbPlacementNotifySink</a>