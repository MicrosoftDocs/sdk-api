---
UID: NF:comsvcs.IComThreadEvents.OnThreadBindToApartment
title: IComThreadEvents::OnThreadBindToApartment
author: windows-sdk-content
description: Generated when an apartment thread is allocated for a single-thread apartment (STA) thread that does not have an apartment thread to run in.
old-location: cos\icomthreadevents_onthreadbindtoapartment.htm
tech.root: cossdk
ms.assetid: d05c784a-5dcd-4155-baa0-775c499bd936
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComThreadEvents interface [COM+],OnThreadBindToApartment method, IComThreadEvents.OnThreadBindToApartment, IComThreadEvents::OnThreadBindToApartment, OnThreadBindToApartment, OnThreadBindToApartment method [COM+], OnThreadBindToApartment method [COM+],IComThreadEvents interface, _dtc_IComThreadEvents_OnThreadBindToApartment, comsvcs/IComThreadEvents::OnThreadBindToApartment, cos.icomthreadevents_onthreadbindtoapartment
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
 - IComThreadEvents.OnThreadBindToApartment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComThreadEvents::OnThreadBindToApartment


## -description


Generated when an apartment thread is allocated for a single-thread apartment (STA) thread that does not have an apartment thread to run in. An apartment thread is created or allocated from the pool.



## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ThreadID [in]

The unique thread identifier.


### -param AptID [in]

The apartment identifier.


### -param dwActCnt [in]

The number of activities bound to this apartment.


### -param dwLowCnt [in]

This parameter is reserved.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685160(v=VS.85).aspx">IComThreadEvents</a>
 

 

