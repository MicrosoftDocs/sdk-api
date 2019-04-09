---
UID: NF:sbtsv.ITsSbPlacementNotifySink.OnQueryEnvironmentCompleted
title: ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted (sbtsv.h)
author: windows-sdk-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the environment specified by the ITsSbClientConnection object is already hosting the correct target.
old-location: termserv\itssbplacementnotifysink_onqueryenvironmentcompleted.htm
tech.root: TermServ
ms.assetid: 937982aa-7655-4681-ba6c-94201743c90c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbPlacementNotifySink interface [Remote Desktop Services],OnQueryEnvironmentCompleted method, ITsSbPlacementNotifySink.OnQueryEnvironmentCompleted, ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted, OnQueryEnvironmentCompleted, OnQueryEnvironmentCompleted method [Remote Desktop Services], OnQueryEnvironmentCompleted method [Remote Desktop Services],ITsSbPlacementNotifySink interface, sbtsv/ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted, termserv.itssbplacementnotifysink_onqueryenvironmentcompleted
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
 - ITsSbPlacementNotifySink.OnQueryEnvironmentCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbPlacementNotifySink::OnQueryEnvironmentCompleted


## -description


Notifies Remote Desktop Connection Broker (RD Connection Broker) that the environment 
specified by the <a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a> object is already hosting the correct target.


## -parameters




### -param pEnvironment [in]

A pointer to an <a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a> environment object. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a>



<a href="https://msdn.microsoft.com/d90501dd-ca15-463c-b204-b1f56103ebe7">ITsSbPlacement</a>



<a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a>
 

 

