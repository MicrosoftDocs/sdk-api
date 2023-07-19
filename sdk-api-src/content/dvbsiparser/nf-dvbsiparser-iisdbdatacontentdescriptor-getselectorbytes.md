---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetSelectorBytes
title: IIsdbDataContentDescriptor::GetSelectorBytes (dvbsiparser.h)
description: Gets the selector data from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. The contents of the selector depend on the type of data transmitted in the data component.
helpviewer_keywords: ["GetSelectorBytes","GetSelectorBytes method [Microsoft TV Technologies]","GetSelectorBytes method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetSelectorBytes method","IIsdbDataContentDescriptor.GetSelectorBytes","IIsdbDataContentDescriptor::GetSelectorBytes","dvbsiparser/IIsdbDataContentDescriptor::GetSelectorBytes","mstv.iisdbdatacontentdescriptor_getselectorbytes"]
old-location: mstv\iisdbdatacontentdescriptor_getselectorbytes.htm
tech.root: mstv
ms.assetid: b02c315e-322d-478e-8be1-c833df49ed56
ms.date: 12/05/2018
ms.keywords: GetSelectorBytes, GetSelectorBytes method [Microsoft TV Technologies], GetSelectorBytes method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetSelectorBytes method, IIsdbDataContentDescriptor.GetSelectorBytes, IIsdbDataContentDescriptor::GetSelectorBytes, dvbsiparser/IIsdbDataContentDescriptor::GetSelectorBytes, mstv.iisdbdatacontentdescriptor_getselectorbytes
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
 - IIsdbDataContentDescriptor::GetSelectorBytes
 - dvbsiparser/IIsdbDataContentDescriptor::GetSelectorBytes
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
 - IIsdbDataContentDescriptor.GetSelectorBytes
---

# IIsdbDataContentDescriptor::GetSelectorBytes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the selector data from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. The contents of the selector depend on the type of data transmitted in the data component.

## -parameters

### -param bBufLength [in]

Specifies the length of the buffer that receives the selector data.

### -param pbBuf [out]

Receives the selector data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Table J-1 in Annex J, <i>SERVICE INFORMATION FOR DIGITAL
BROADCASTING SYSTEM
ARIB STANDARD
ARIB, STD-B10, Version 4.6</i> shows the contents of this descriptor for different component types.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>