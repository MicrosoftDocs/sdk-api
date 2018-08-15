---
UID: NF:tuner.IDVBTLocator.get_Guard
title: IDVBTLocator::get_Guard
author: windows-sdk-content
description: The get_Guard method retrieves the guard interval.
old-location: mstv\idvbtlocator_get_guard.htm
old-project: mstv
ms.assetid: 74b56292-eb9e-4c66-9345-f348b3d21c19
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_Guard method, IDVBTLocator.get_Guard, IDVBTLocator::get_Guard, IDVBTLocatorget_Guard, get_Guard, get_Guard method [Microsoft TV Technologies], get_Guard method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_guard, tuner/IDVBTLocator::get_Guard
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBTLocator.get_Guard
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTLocator::get_Guard


## -description



The <b>get_Guard</b> method retrieves the guard interval.




## -parameters




### -param GI






#### - pGI [out]

Receives a member of the <a href="https://msdn.microsoft.com/a3ff1c61-f80d-40f2-a22f-069f0690fb1b">GuardInterval</a> enumeration.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

