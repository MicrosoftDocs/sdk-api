---
UID: NF:tuner.IESEvent.GetEventId
title: IESEvent::GetEventId (tuner.h)
author: windows-sdk-content
description: Gets the unique identifier from an event that is derived from the IESEvent interface. The event identifier is contained in an IESEvent object, which ispassed in a call to IESEventService::FireESEvent.
old-location: mstv\iesevent_geteventid.htm
tech.root: mstv
ms.assetid: 8a7d62de-71fc-40fa-9944-d41e33243cc5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEventId, GetEventId method [Microsoft TV Technologies], GetEventId method [Microsoft TV Technologies],IESEvent interface, IESEvent interface [Microsoft TV Technologies],GetEventId method, IESEvent.GetEventId, IESEvent::GetEventId, mstv.iesevent_geteventid, tuner/IESEvent::GetEventId
ms.topic: method
f1_keywords: ["tuner/IESEvent.GetEventId"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEvent::GetEventId


## -description


Gets the unique identifier from an event that is derived from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. The event identifier is contained in an <b>IESEvent</b> object, which ispassed in a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">IESEventService::FireESEvent</a>.


## -parameters




### -param pdwEventId [out, retval]

Receives the event identifier.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">FireESEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>
 

 

