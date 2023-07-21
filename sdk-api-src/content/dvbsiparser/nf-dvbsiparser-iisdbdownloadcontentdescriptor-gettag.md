---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetTag
title: IIsdbDownloadContentDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbDownloadContentDescriptor.GetTag","IIsdbDownloadContentDescriptor::GetTag","dvbsiparser/IIsdbDownloadContentDescriptor::GetTag","mstv.iisdbdownloadcontentdescriptor_gettag"]
old-location: mstv\iisdbdownloadcontentdescriptor_gettag.htm
tech.root: mstv
ms.assetid: a78c3f3b-aaa2-4b5e-9cf8-7746f20fafc2
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbDownloadContentDescriptor.GetTag, IIsdbDownloadContentDescriptor::GetTag, dvbsiparser/IIsdbDownloadContentDescriptor::GetTag, mstv.iisdbdownloadcontentdescriptor_gettag
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
 - IIsdbDownloadContentDescriptor::GetTag
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetTag
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
 - IIsdbDownloadContentDescriptor.GetTag
---

# IIsdbDownloadContentDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) download content descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For ISDB download content descriptors, this value is 0xC9.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>