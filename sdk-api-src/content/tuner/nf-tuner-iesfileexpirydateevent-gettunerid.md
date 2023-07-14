---
UID: NF:tuner.IESFileExpiryDateEvent.GetTunerId
title: IESFileExpiryDateEvent::GetTunerId (tuner.h)
description: Gets a globally unique identifier (GUID) from a FileExpiryDate event that identifies the media transform device (MTD) that originated the event.
helpviewer_keywords: ["GetTunerId","GetTunerId method [Microsoft TV Technologies]","GetTunerId method [Microsoft TV Technologies]","IESFileExpiryDateEvent interface","IESFileExpiryDateEvent interface [Microsoft TV Technologies]","GetTunerId method","IESFileExpiryDateEvent.GetTunerId","IESFileExpiryDateEvent::GetTunerId","mstv.iesfileexpirydateevent_gettunerid","tuner/IESFileExpiryDateEvent::GetTunerId"]
old-location: mstv\iesfileexpirydateevent_gettunerid.htm
tech.root: mstv
ms.assetid: 1271df60-7830-4e10-9af8-caf59aff56f8
ms.date: 12/05/2018
ms.keywords: GetTunerId, GetTunerId method [Microsoft TV Technologies], GetTunerId method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],GetTunerId method, IESFileExpiryDateEvent.GetTunerId, IESFileExpiryDateEvent::GetTunerId, mstv.iesfileexpirydateevent_gettunerid, tuner/IESFileExpiryDateEvent::GetTunerId
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
 - IESFileExpiryDateEvent::GetTunerId
 - tuner/IESFileExpiryDateEvent::GetTunerId
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
 - IESFileExpiryDateEvent.GetTunerId
---

# IESFileExpiryDateEvent::GetTunerId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a  globally unique identifier (GUID) from a <b>FileExpiryDate</b> event that identifies the media transform device (MTD) that originated the event.

## -parameters

### -param pguidTunerId [out, retval]

Receives the GUID for the MTD.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesfileexpirydateevent">IESFileExpiryDateEvent</a>