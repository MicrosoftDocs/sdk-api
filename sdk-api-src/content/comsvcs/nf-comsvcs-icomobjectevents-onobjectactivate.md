---
UID: NF:comsvcs.IComObjectEvents.OnObjectActivate
title: IComObjectEvents::OnObjectActivate
author: windows-sdk-content
description: Generated when an object gets an instance of a new JIT-activated object.
old-location: cos\icomobjectevents_onobjectactivate.htm
tech.root: cossdk
ms.assetid: 149e3820-0d5b-46ee-9be9-22850115a7c7
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IComObjectEvents interface [COM+],OnObjectActivate method, IComObjectEvents.OnObjectActivate, IComObjectEvents::OnObjectActivate, OnObjectActivate, OnObjectActivate method [COM+], OnObjectActivate method [COM+],IComObjectEvents interface, _dtc_IComObjectEvents_OnObjectActivate, comsvcs/IComObjectEvents::OnObjectActivate, cos.icomobjectevents_onobjectactivate
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IComObjectEvents.OnObjectActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectEvents::OnObjectActivate


## -description


Generated when an object gets an instance of a new JIT-activated object.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param CtxtID [in]

The GUID of the current context.


### -param ObjectID [in]

The JIT-activated object.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1">IComObjectEvents</a>
 

 

