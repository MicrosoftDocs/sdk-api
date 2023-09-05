---
UID: NF:tuner.IESEvent.GetData
title: IESEvent::GetData (tuner.h)
description: Gets data from an event that is derived from the IESEvent interface. This method gets a byte array that contains the data in an IESEvent object, which is passed in a call to IESEventService::FireESEvent.
helpviewer_keywords: ["GetData","GetData method [Microsoft TV Technologies]","GetData method [Microsoft TV Technologies]","IESEvent interface","IESEvent interface [Microsoft TV Technologies]","GetData method","IESEvent.GetData","IESEvent::GetData","mstv.iesevent_getdata","tuner/IESEvent::GetData"]
old-location: mstv\iesevent_getdata.htm
tech.root: mstv
ms.assetid: bef529c5-0a97-4eb0-83ca-669edc7a2452
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Microsoft TV Technologies], GetData method [Microsoft TV Technologies],IESEvent interface, IESEvent interface [Microsoft TV Technologies],GetData method, IESEvent.GetData, IESEvent::GetData, mstv.iesevent_getdata, tuner/IESEvent::GetData
f1_keywords:
- tuner/IESEvent.GetData
dev_langs:
- c++
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
- IESEvent.GetData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESEvent::GetData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]


Gets data from an event that is derived from the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a> interface. This method gets a byte array that contains the data in an <b>IESEvent</b> object, which is passed in a call to <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">IESEventService::FireESEvent</a>.


## -parameters




### -param pbData [out, retval]

Pointer to <b>SAFEARRAY</b> that receives the event data.
          The caller is responsible for freeing the <b>SAFEARRAY</b>.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieseventservice-fireesevent">FireESEvent</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>
 

 