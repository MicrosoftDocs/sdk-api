---
UID: NF:qnetwork.IAMExtendedSeeking.GetMarkerTime
title: IAMExtendedSeeking::GetMarkerTime
author: windows-sdk-content
description: The GetMarkerTime method retrieves the presentation time associated with the specified marker.
old-location: dshow\iamextendedseeking_getmarkertime.htm
tech.root: DirectShow
ms.assetid: 719e87c5-7d38-4b02-8342-055e42405511
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetMarkerTime, GetMarkerTime method [DirectShow], GetMarkerTime method [DirectShow],IAMExtendedSeeking interface, IAMExtendedSeeking interface [DirectShow],GetMarkerTime method, IAMExtendedSeeking.GetMarkerTime, IAMExtendedSeeking::GetMarkerTime, IAMExtendedSeekingGetMarkerTime, dshow.iamextendedseeking_getmarkertime, qnetwork/IAMExtendedSeeking::GetMarkerTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qnetwork.h
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
 - Qnetwork.h
api_name:
 - IAMExtendedSeeking.GetMarkerTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtendedSeeking::GetMarkerTime


## -description



The <b>GetMarkerTime</b> method retrieves the presentation time associated with the specified marker.




## -parameters




### -param MarkerNum [in]

Specifies the marker number.


### -param pMarkerTime [out]

Pointer to a variable that receives the marker time.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9e0e49af-61ef-408c-8c26-bb29ab26a1f5">IAMExtendedSeeking Interface</a>



<a href="https://msdn.microsoft.com/899cc32e-3a9f-4be0-97a9-2ddd323bf9ce">IAMExtendedSeeking::GetMarkerName</a>
 

 

