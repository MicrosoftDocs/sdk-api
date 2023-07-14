---
UID: NF:tuner.IESIsdbCasResponseEvent.GetResponseData
title: IESIsdbCasResponseEvent::GetResponseData (tuner.h)
description: Gets the response data returned in an IsdbCasResponse event.
helpviewer_keywords: ["GetResponseData","GetResponseData method [DirectShow]","GetResponseData method [DirectShow]","IESIsdbCasResponseEvent interface","IESIsdbCasResponseEvent interface [DirectShow]","GetResponseData method","IESIsdbCasResponseEvent.GetResponseData","IESIsdbCasResponseEvent::GetResponseData","mstv.iesisdbcasresponseevent_getresponsedata","tuner/IESIsdbCasResponseEvent::GetResponseData"]
old-location: mstv\iesisdbcasresponseevent_getresponsedata.htm
tech.root: mstv
ms.assetid: ee0618a6-6162-4178-be44-978558add914
ms.date: 12/05/2018
ms.keywords: GetResponseData, GetResponseData method [DirectShow], GetResponseData method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetResponseData method, IESIsdbCasResponseEvent.GetResponseData, IESIsdbCasResponseEvent::GetResponseData, mstv.iesisdbcasresponseevent_getresponsedata, tuner/IESIsdbCasResponseEvent::GetResponseData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IESIsdbCasResponseEvent::GetResponseData
 - tuner/IESIsdbCasResponseEvent::GetResponseData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESIsdbCasResponseEvent.GetResponseData
---

# IESIsdbCasResponseEvent::GetResponseData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the response data returned in an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IsdbCasResponse</a> event.

## -parameters

### -param pbData [out, retval]

Pointer to a buffer that receives the response data. The caller must free this memory after use.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IESIsdbCasResponseEvent</a>