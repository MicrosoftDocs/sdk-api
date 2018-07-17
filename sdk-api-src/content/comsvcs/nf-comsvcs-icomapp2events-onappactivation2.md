---
UID: NF:comsvcs.IComApp2Events.OnAppActivation2
title: IComApp2Events::OnAppActivation2
author: windows-sdk-content
description: Generated when the server application process is loaded.
old-location: cos\icomapp2events_onappactivation2.htm
old-project: cossdk
ms.assetid: d621f46e-19c2-4fab-8820-a5716cb7cdc4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IComApp2Events interface [COM+],OnAppActivation2 method, IComApp2Events.OnAppActivation2, IComApp2Events::OnAppActivation2, OnAppActivation2, OnAppActivation2 method [COM+], OnAppActivation2 method [COM+],IComApp2Events interface, _dtc_IComApp2Events_OnAppActivation2, comsvcs/IComApp2Events::OnAppActivation2, cos.icomapp2events_onappactivation2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IComApp2Events.OnAppActivation2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComApp2Events::OnAppActivation2


## -description


Generated when the server application process is loaded.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The GUID of the application.


### -param guidProcess [in]

The process ID.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/45e0d26b-7485-436b-9b64-fa48217b32d1">IComApp2Events</a>
 

 

