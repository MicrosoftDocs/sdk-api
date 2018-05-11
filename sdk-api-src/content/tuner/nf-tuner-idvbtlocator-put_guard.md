---
UID: NF:tuner.IDVBTLocator.put_Guard
title: IDVBTLocator::put_Guard
author: windows-driver-content
description: The put_Guard method sets the guard interval.
old-location: mstv\idvbtlocator_put_guard.htm
old-project: mstv
ms.assetid: af0accaf-ef33-4074-ac04-2bd09f3ad879
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_Guard method, IDVBTLocator.put_Guard, IDVBTLocator::put_Guard, IDVBTLocatorput_Guard, mstv.idvbtlocator_put_guard, put_Guard, put_Guard method [Microsoft TV Technologies], put_Guard method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_Guard
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IDVBTLocator.put_Guard
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBTLocator::put_Guard


## -description



The <b>put_Guard</b> method sets the guard interval.




## -parameters




### -param GI [in]

Variable of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff559626">GuardInterval</a> that specifies the guard interval.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/f5a95a68-fee0-404c-b9c6-6b808977f8d2">IDVBTLocator Interface</a>
 

 

