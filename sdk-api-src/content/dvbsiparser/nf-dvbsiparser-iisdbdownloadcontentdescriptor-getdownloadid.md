---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetDownloadId
title: IIsdbDownloadContentDescriptor::GetDownloadId (dvbsiparser.h)
description: Gets the download identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The download identifier identifies an application number for the download.
helpviewer_keywords: ["GetDownloadId","GetDownloadId method [Microsoft TV Technologies]","GetDownloadId method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetDownloadId method","IIsdbDownloadContentDescriptor.GetDownloadId","IIsdbDownloadContentDescriptor::GetDownloadId","dvbsiparser/IIsdbDownloadContentDescriptor::GetDownloadId","mstv.iisdbdownloadcontentdescriptor_getdownloadid"]
old-location: mstv\iisdbdownloadcontentdescriptor_getdownloadid.htm
tech.root: mstv
ms.assetid: b57eba56-b9d6-4555-8d5d-80fd2b9fd23f
ms.date: 12/05/2018
ms.keywords: GetDownloadId, GetDownloadId method [Microsoft TV Technologies], GetDownloadId method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetDownloadId method, IIsdbDownloadContentDescriptor.GetDownloadId, IIsdbDownloadContentDescriptor::GetDownloadId, dvbsiparser/IIsdbDownloadContentDescriptor::GetDownloadId, mstv.iisdbdownloadcontentdescriptor_getdownloadid
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
 - IIsdbDownloadContentDescriptor::GetDownloadId
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetDownloadId
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
 - IIsdbDownloadContentDescriptor.GetDownloadId
---

# IIsdbDownloadContentDescriptor::GetDownloadId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the download identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The download identifier identifies an application number for the download.

## -parameters

### -param pdwVal [out]

Receives the download identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>