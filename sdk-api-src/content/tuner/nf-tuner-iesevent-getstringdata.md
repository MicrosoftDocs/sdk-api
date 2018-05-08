---
UID: NF:tuner.IESEvent.GetStringData
title: IESEvent::GetStringData
author: windows-driver-content
description: Gets the data from an event that is derived from the IESEvent interface, in Unicode string format. The data is contained in an IESEvent object, which ispassed in a call to IESEventService::FireESEvent.
old-location: mstv\iesevent_getstringdata.htm
old-project: mstv
ms.assetid: 6a1c98af-a753-40e5-bea8-825863f94172
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetStringData, GetStringData method [Microsoft TV Technologies], GetStringData method [Microsoft TV Technologies],IESEvent interface, IESEvent interface [Microsoft TV Technologies],GetStringData method, IESEvent.GetStringData, IESEvent::GetStringData, mstv.iesevent_getstringdata, tuner/IESEvent::GetStringData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
-	IESEvent.GetStringData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEvent::GetStringData


## -description



      Gets the data from an event  that is derived from the <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> interface, in Unicode string format. The data is contained in an <b>IESEvent</b> object, which ispassed in a call to <a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">IESEventService::FireESEvent</a>.


## -parameters




### -param pbstrData [out, retval]


            Pointer to a buffer that receives the data that is passed with the <b>IESEvent</b> object, in Unicode string format. The caller must release this memory.

          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">FireESEvent</a>



<a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>
 

 

