---
UID: NF:comsvcs.IComApp2Events.OnAppForceShutdown2
title: IComApp2Events::OnAppForceShutdown2
author: windows-sdk-content
description: Generated when the server application is forced to shut down.
old-location: cos\icomapp2events_onappforceshutdown2.htm
old-project: cossdk
ms.assetid: 7658caaa-a995-4b88-a314-b5cd981d1ec6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComApp2Events interface [COM+],OnAppForceShutdown2 method, IComApp2Events.OnAppForceShutdown2, IComApp2Events::OnAppForceShutdown2, OnAppForceShutdown2, OnAppForceShutdown2 method [COM+], OnAppForceShutdown2 method [COM+],IComApp2Events interface, _dtc_IComApp2Events_OnAppForceShutdown2, comsvcs/IComApp2Events::OnAppForceShutdown2, cos.icomapp2events_onappforceshutdown2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
 - IComApp2Events.OnAppForceShutdown2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComApp2Events::OnAppForceShutdown2


## -description


Generated when the server application is forced to shut down.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The GUID of the application.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/45e0d26b-7485-436b-9b64-fa48217b32d1">IComApp2Events</a>
 

 

