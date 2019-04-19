---
UID: NF:comsvcs.IComObjectEvents.OnSetComplete
title: IComObjectEvents::OnSetComplete (comsvcs.h)
author: windows-sdk-content
description: Generated when the client calls SetComplete on a context.
old-location: cos\icomobjectevents_onsetcomplete.htm
tech.root: cossdk
ms.assetid: 3bda05b7-3306-428c-b920-d87eee0b35d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComObjectEvents interface [COM+],OnSetComplete method, IComObjectEvents.OnSetComplete, IComObjectEvents::OnSetComplete, OnSetComplete, OnSetComplete method [COM+], OnSetComplete method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnSetComplete, comsvcs/IComObjectEvents::OnSetComplete, cos.icomobjectevents_onsetcomplete
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
 - IComObjectEvents.OnSetComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComObjectEvents::OnSetComplete


## -description


Generated when the client calls <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a> on a context.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The GUID of the current context.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1">IComObjectEvents</a>
 

 

