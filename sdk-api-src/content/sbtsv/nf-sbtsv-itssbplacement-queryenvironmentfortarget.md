---
UID: NF:sbtsv.ITsSbPlacement.QueryEnvironmentForTarget
title: ITsSbPlacement::QueryEnvironmentForTarget
author: windows-sdk-content
description: Determines whether the specified environment is ready to host the target that was returned by load balancing.
old-location: termserv\itssbplacement_queryenvironmentfortarget.htm
tech.root: termserv
ms.assetid: 62320a0b-3f3e-4341-a481-a43af39c06f7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbPlacement interface [Remote Desktop Services],QueryEnvironmentForTarget method, ITsSbPlacement.QueryEnvironmentForTarget, ITsSbPlacement::QueryEnvironmentForTarget, QueryEnvironmentForTarget, QueryEnvironmentForTarget method [Remote Desktop Services], QueryEnvironmentForTarget method [Remote Desktop Services],ITsSbPlacement interface, sbtsv/ITsSbPlacement::QueryEnvironmentForTarget, termserv.itssbplacement_queryenvironmentfortarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ITsSbPlacement.QueryEnvironmentForTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbPlacement::QueryEnvironmentForTarget


## -description


Determines whether the specified environment is ready to host 
the target that was returned by load balancing.


## -parameters




### -param pConnection [in]

A pointer to an <a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a> client connection object.


### -param pPlacementSink [in]

 A pointer to an <a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a> placement sink object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Your plug-in should use the <a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a> object to report the state of the environment to Remote Desktop Connection Broker (RD Connection Broker).

After RD Connection Broker receives a load-balancing result, it calls <b>QueryEnvironmentForTarget</b> 
to determine whether the environment is present and ready.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/d90501dd-ca15-463c-b204-b1f56103ebe7">ITsSbPlacement</a>



<a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a>
 

 

