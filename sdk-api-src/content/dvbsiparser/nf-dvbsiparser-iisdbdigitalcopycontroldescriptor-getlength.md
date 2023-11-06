---
UID: NF:dvbsiparser.IIsdbDigitalCopyControlDescriptor.GetLength
title: IIsdbDigitalCopyControlDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IIsdbDigitalCopyControlDescriptor interface","IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies]","GetLength method","IIsdbDigitalCopyControlDescriptor.GetLength","IIsdbDigitalCopyControlDescriptor::GetLength","dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetLength","mstv.iisdbdigitalcopycontroldescriptor_getlength"]
old-location: mstv\iisdbdigitalcopycontroldescriptor_getlength.htm
tech.root: mstv
ms.assetid: 3a0b5433-1681-4b2d-9436-9ed853da6a80
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbDigitalCopyControlDescriptor interface, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbDigitalCopyControlDescriptor.GetLength, IIsdbDigitalCopyControlDescriptor::GetLength, dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetLength, mstv.iisdbdigitalcopycontroldescriptor_getlength
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IIsdbDigitalCopyControlDescriptor::GetLength
 - dvbsiparser/IIsdbDigitalCopyControlDescriptor::GetLength
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
 - IIsdbDigitalCopyControlDescriptor.GetLength
---

# IIsdbDigitalCopyControlDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor, in bytes.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdigitalcopycontroldescriptor">IIsdbDigitalCopyControlDescriptor</a>