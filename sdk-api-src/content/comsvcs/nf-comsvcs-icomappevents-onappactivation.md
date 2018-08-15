---
UID: NF:comsvcs.IComAppEvents.OnAppActivation
title: IComAppEvents::OnAppActivation
author: windows-sdk-content
description: Generated when an application server starts.
old-location: cos\icomappevents_onappactivation.htm
old-project: cossdk
ms.assetid: 4561d15a-6c1b-48e7-9697-87dfb51f877c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IComAppEvents interface [COM+],OnAppActivation method, IComAppEvents.OnAppActivation, IComAppEvents::OnAppActivation, OnAppActivation, OnAppActivation method [COM+], OnAppActivation method [COM+],IComAppEvents interface, _dtc_IComAppEvents_OnAppActivation, comsvcs/IComAppEvents::OnAppActivation, cos.icomappevents_onappactivation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComAppEvents.OnAppActivation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComAppEvents::OnAppActivation


## -description


Generated when an application server starts.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The globally unique identifier (GUID) of the application.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/61ae1926-601b-4d97-80e4-d2d2098ced39">IComAppEvents</a>
 

 

