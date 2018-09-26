---
UID: NF:comsvcs.IComThreadEvents.OnThreadTerminate
title: IComThreadEvents::OnThreadTerminate
author: windows-sdk-content
description: Generated when a single-threaded apartment (STA) thread is terminated.
old-location: cos\icomthreadevents_onthreadterminate.htm
tech.root: cossdk
ms.assetid: 8483962c-46c9-4ef1-8c7e-391a04334293
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadTerminate method, IComThreadEvents.OnThreadTerminate, IComThreadEvents::OnThreadTerminate, OnThreadTerminate, OnThreadTerminate method [COM+], OnThreadTerminate method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadTerminate, comsvcs/IComThreadEvents::OnThreadTerminate, cos.icomthreadevents_onthreadterminate
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
 - IComThreadEvents.OnThreadTerminate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComThreadEvents::OnThreadTerminate


## -description


Generated when a single-threaded apartment (STA) thread is terminated.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ThreadID [in]

The unique thread identifier.


### -param dwThread [in]

The Windows thread identifier.


### -param dwTheadCnt [in]

The number of threads in the STA thread pool.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/a6523088-cca4-41c1-a3fe-d8cb7320ff33">IComThreadEvents</a>
 

 

