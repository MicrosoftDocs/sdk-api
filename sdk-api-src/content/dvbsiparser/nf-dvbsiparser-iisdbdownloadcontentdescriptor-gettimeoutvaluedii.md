---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetTimeOutValueDII
title: IIsdbDownloadContentDescriptor::GetTimeOutValueDII (dvbsiparser.h)
description: Gets the value of the time_out_value_DII field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
helpviewer_keywords: ["GetTimeOutValueDII","GetTimeOutValueDII method [Microsoft TV Technologies]","GetTimeOutValueDII method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetTimeOutValueDII method","IIsdbDownloadContentDescriptor.GetTimeOutValueDII","IIsdbDownloadContentDescriptor::GetTimeOutValueDII","dvbsiparser/IIsdbDownloadContentDescriptor::GetTimeOutValueDII","mstv.iisdbdownloadcontentdescriptor_gettimeoutvaluedii"]
old-location: mstv\iisdbdownloadcontentdescriptor_gettimeoutvaluedii.htm
tech.root: mstv
ms.assetid: ec1bd153-e637-4046-8d7b-f2868c4909dd
ms.date: 12/05/2018
ms.keywords: GetTimeOutValueDII, GetTimeOutValueDII method [Microsoft TV Technologies], GetTimeOutValueDII method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetTimeOutValueDII method, IIsdbDownloadContentDescriptor.GetTimeOutValueDII, IIsdbDownloadContentDescriptor::GetTimeOutValueDII, dvbsiparser/IIsdbDownloadContentDescriptor::GetTimeOutValueDII, mstv.iisdbdownloadcontentdescriptor_gettimeoutvaluedii
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
 - IIsdbDownloadContentDescriptor::GetTimeOutValueDII
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetTimeOutValueDII
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
 - IIsdbDownloadContentDescriptor.GetTimeOutValueDII
---

# IIsdbDownloadContentDescriptor::GetTimeOutValueDII


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the  value of the time_out_value_DII field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The time_out_value_DII field indicates the recommended timeout value  for receiving all sections of the corresponding carousel, in milliseconds.

## -parameters

### -param pdwVal [out]

Receives the recommended timeout value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>