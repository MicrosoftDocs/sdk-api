---
UID: NF:comsvcs.IComObjectEvents.OnEnableCommit
title: IComObjectEvents::OnEnableCommit
author: windows-sdk-content
description: Generated when the client calls EnableCommit on a context.
old-location: cos\icomobjectevents_onenablecommit.htm
tech.root: cossdk
ms.assetid: 88fdf857-1dbd-4a6b-87c6-0d72eeeab9b4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComObjectEvents interface [COM+],OnEnableCommit method, IComObjectEvents.OnEnableCommit, IComObjectEvents::OnEnableCommit, OnEnableCommit, OnEnableCommit method [COM+], OnEnableCommit method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnEnableCommit, comsvcs/IComObjectEvents::OnEnableCommit, cos.icomobjectevents_onenablecommit
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ComSvcs.h
api_name:
 - IComObjectEvents.OnEnableCommit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectEvents::OnEnableCommit


## -description


Generated when the client calls <a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">EnableCommit</a> on a context.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The GUID of the current context.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1">IComObjectEvents</a>
 

 

