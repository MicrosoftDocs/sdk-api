---
UID: NF:comsvcs.IComInstanceEvents.OnObjectDestroy
title: IComInstanceEvents::OnObjectDestroy (comsvcs.h)
author: windows-sdk-content
description: Generated when an object is released by a client.
old-location: cos\icominstanceevents_onobjectdestroy.htm
tech.root: cossdk
ms.assetid: 3eea4171-a177-4adc-bd9a-856a558ba3d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComInstanceEvents interface [COM+],OnObjectDestroy method, IComInstanceEvents.OnObjectDestroy, IComInstanceEvents::OnObjectDestroy, OnObjectDestroy, OnObjectDestroy method [COM+], OnObjectDestroy method [COM+],IComInstanceEvents interface, _dtc_IComInstanceEvents_OnObjectDestroy, comsvcs/IComInstanceEvents::OnObjectDestroy, cos.icominstanceevents_onobjectdestroy
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
 - IComInstanceEvents.OnObjectDestroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComInstanceEvents::OnObjectDestroy


## -description


Generated when an object is released by a client.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The context identifier of the object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icominstanceevents">IComInstanceEvents</a>
 

 

