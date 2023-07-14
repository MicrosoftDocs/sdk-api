---
UID: NF:tuner.IESIsdbCasResponseEvent.GetRequestId
title: IESIsdbCasResponseEvent::GetRequestId (tuner.h)
description: Gets the request identifier returned in an IsdbCasResponse event. The request identifier identifies the request originated by a PBDA media sink device (MSD).
helpviewer_keywords: ["GetRequestId","GetRequestId method [DirectShow]","GetRequestId method [DirectShow]","IESIsdbCasResponseEvent interface","IESIsdbCasResponseEvent interface [DirectShow]","GetRequestId method","IESIsdbCasResponseEvent.GetRequestId","IESIsdbCasResponseEvent::GetRequestId","mstv.iesisdbcasresponseevent_getrequestid","tuner/IESIsdbCasResponseEvent::GetRequestId"]
old-location: mstv\iesisdbcasresponseevent_getrequestid.htm
tech.root: mstv
ms.assetid: b3ab39b4-567f-49a5-b3d2-460ec648ab26
ms.date: 12/05/2018
ms.keywords: GetRequestId, GetRequestId method [DirectShow], GetRequestId method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetRequestId method, IESIsdbCasResponseEvent.GetRequestId, IESIsdbCasResponseEvent::GetRequestId, mstv.iesisdbcasresponseevent_getrequestid, tuner/IESIsdbCasResponseEvent::GetRequestId
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
 - IESIsdbCasResponseEvent::GetRequestId
 - tuner/IESIsdbCasResponseEvent::GetRequestId
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
 - IESIsdbCasResponseEvent.GetRequestId
---

# IESIsdbCasResponseEvent::GetRequestId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the request identifier returned in an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IsdbCasResponse</a> event. The request identifier identifies the request originated by a PBDA media sink device (MSD).

## -parameters

### -param pRequestId [out, retval]

Receives the request identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IESIsdbCasResponseEvent</a>