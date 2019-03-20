---
UID: NF:comsvcs.IComObjectEvents.OnDisableCommit
title: IComObjectEvents::OnDisableCommit (comsvcs.h)
author: windows-sdk-content
description: Generated when the client calls DisableCommit on a context.
old-location: cos\icomobjectevents_ondisablecommit.htm
tech.root: cossdk
ms.assetid: 413d7216-294c-4e46-b24c-abe1d1a09239
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComObjectEvents interface [COM+],OnDisableCommit method, IComObjectEvents.OnDisableCommit, IComObjectEvents::OnDisableCommit, OnDisableCommit, OnDisableCommit method [COM+], OnDisableCommit method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnDisableCommit, comsvcs/IComObjectEvents::OnDisableCommit, cos.icomobjectevents_ondisablecommit
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
 - IComObjectEvents.OnDisableCommit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectEvents::OnDisableCommit


## -description


Generated when the client calls <a href="https://msdn.microsoft.com/e83d1223-9b8e-4a92-b98d-9d2b6ed34721">DisableCommit</a> on a context.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The GUID of the current context.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1">IComObjectEvents</a>
 

 

