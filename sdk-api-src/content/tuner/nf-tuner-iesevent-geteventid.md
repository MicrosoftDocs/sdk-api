---
UID: NF:tuner.IESEvent.GetEventId
title: IESEvent::GetEventId
author: windows-sdk-content
description: Gets the unique identifier from an event that is derived from the IESEvent interface. The event identifier is contained in an IESEvent object, which ispassed in a call to IESEventService::FireESEvent.
old-location: mstv\iesevent_geteventid.htm
old-project: mstv
ms.assetid: 8a7d62de-71fc-40fa-9944-d41e33243cc5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEventId, GetEventId method [Microsoft TV Technologies], GetEventId method [Microsoft TV Technologies],IESEvent interface, IESEvent interface [Microsoft TV Technologies],GetEventId method, IESEvent.GetEventId, IESEvent::GetEventId, mstv.iesevent_geteventid, tuner/IESEvent::GetEventId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
 - IESEvent.GetEventId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESEvent::GetEventId


## -description


Gets the unique identifier from an event that is derived from the <a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a> interface. The event identifier is contained in an <b>IESEvent</b> object, which ispassed in a call to <a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">IESEventService::FireESEvent</a>.


## -parameters




### -param pdwEventId [out, retval]

Receives the event identifier.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3781e50c-ab19-4bfa-86d6-af12223019ca">FireESEvent</a>



<a href="https://msdn.microsoft.com/3c375480-c6df-4bb0-b417-5765b0bed9bf">IESEvent</a>
 

 

