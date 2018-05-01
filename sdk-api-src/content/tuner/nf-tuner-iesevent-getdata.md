---
UID: NF:tuner.IESEvent.GetData
title: IESEvent::GetData method
author: windows-driver-content
description: Gets data from an event that is derived from the IESEvent interface. This method gets a byte array that contains the data in an IESEvent object, which is passed in a call to IESEventService::FireESEvent.
old-location: mstv\iesevent_getdata.htm
old-project: mstv
ms.assetid: bef529c5-0a97-4eb0-83ca-669edc7a2452
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetData method [Microsoft TV Technologies], GetData method [Microsoft TV Technologies], IESEvent interface, GetData,IESEvent.GetData, IESEvent, IESEvent interface [Microsoft TV Technologies], GetData method, IESEvent::GetData, mstv.iesevent_getdata, tuner/IESEvent::GetData
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
-	IESEvent.GetData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEvent::GetData method


## -description



      Gets data from an event that is derived from the <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> interface. This method gets a byte array that contains the data in an <b>IESEvent</b> object, which is passed in a call to <a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">IESEventService::FireESEvent</a>.


## -parameters




### -param pbData [out, retval]


            Pointer to <b>SAFEARRAY</b> that receives the event data.
          The caller is responsible for freeing the <b>SAFEARRAY</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">FireESEvent</a>



<a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>
 

 

