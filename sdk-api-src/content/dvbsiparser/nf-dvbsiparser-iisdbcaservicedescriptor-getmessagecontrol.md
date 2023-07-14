---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetMessageControl
title: IIsdbCAServiceDescriptor::GetMessageControl (dvbsiparser.h)
description: Gets the delay time, in days, before the automatic entitlement management message (EMM) is displayed from a conditional access (CA) service descriptor.
helpviewer_keywords: ["GetMessageControl","GetMessageControl method [Microsoft TV Technologies]","GetMessageControl method [Microsoft TV Technologies]","IIsdbCAServiceDescriptor interface","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","GetMessageControl method","IIsdbCAServiceDescriptor.GetMessageControl","IIsdbCAServiceDescriptor::GetMessageControl","dvbsiparser/IIsdbCAServiceDescriptor::GetMessageControl","mstv.iisdbcaservicedescriptor_getmessagecontrol"]
old-location: mstv\iisdbcaservicedescriptor_getmessagecontrol.htm
tech.root: mstv
ms.assetid: 0a911c5e-a026-4d35-a6a2-e33ba53f3057
ms.date: 12/05/2018
ms.keywords: GetMessageControl, GetMessageControl method [Microsoft TV Technologies], GetMessageControl method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetMessageControl method, IIsdbCAServiceDescriptor.GetMessageControl, IIsdbCAServiceDescriptor::GetMessageControl, dvbsiparser/IIsdbCAServiceDescriptor::GetMessageControl, mstv.iisdbcaservicedescriptor_getmessagecontrol
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbCAServiceDescriptor::GetMessageControl
 - dvbsiparser/IIsdbCAServiceDescriptor::GetMessageControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbCAServiceDescriptor.GetMessageControl
---

# IIsdbCAServiceDescriptor::GetMessageControl


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the delay time, in days, before the automatic  entitlement management message (EMM) is displayed from a conditional access (CA) service descriptor.

## -parameters

### -param pbVal [out]

Receives the number of days before the EMM message is displayed. A value of 0xFF indicates that the delay time is
disabled (that the start of the delay time has been put on hold).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When playing a previously received and stored program on a receiver with stored
reception functionality, a least significant bit of 1 in this field indicates that the
automatic display message will not be displayed.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcaservicedescriptor">IIsdbCAServiceDescriptor</a>