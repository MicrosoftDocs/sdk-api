---
UID: NF:tuner.IESIsdbCasResponseEvent.GetDataLength
title: IESIsdbCasResponseEvent::GetDataLength (tuner.h)
description: Gets the length of response data returned in anIsdbCasResponse event.
helpviewer_keywords: ["GetDataLength","GetDataLength method [DirectShow]","GetDataLength method [DirectShow]","IESIsdbCasResponseEvent interface","IESIsdbCasResponseEvent interface [DirectShow]","GetDataLength method","IESIsdbCasResponseEvent.GetDataLength","IESIsdbCasResponseEvent::GetDataLength","mstv.iesisdbcasresponseevent_getdatalength","tuner/IESIsdbCasResponseEvent::GetDataLength"]
old-location: mstv\iesisdbcasresponseevent_getdatalength.htm
tech.root: mstv
ms.assetid: dc625c6f-84e8-4a82-b53c-717b33c10d04
ms.date: 12/05/2018
ms.keywords: GetDataLength, GetDataLength method [DirectShow], GetDataLength method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetDataLength method, IESIsdbCasResponseEvent.GetDataLength, IESIsdbCasResponseEvent::GetDataLength, mstv.iesisdbcasresponseevent_getdatalength, tuner/IESIsdbCasResponseEvent::GetDataLength
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
 - IESIsdbCasResponseEvent::GetDataLength
 - tuner/IESIsdbCasResponseEvent::GetDataLength
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
 - IESIsdbCasResponseEvent.GetDataLength
---

# IESIsdbCasResponseEvent::GetDataLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length of response data returned in an<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IsdbCasResponse</a> event.

## -parameters

### -param pRequestLength [out, retval]

Receives the length of the response data, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesisdbcasresponseevent">IESIsdbCasResponseEvent</a>