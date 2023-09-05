---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetCompatiblityDescriptorLength
title: IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength (dvbsiparser.h)
description: Gets the length of the compatibility descriptor from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
helpviewer_keywords: ["GetCompatiblityDescriptorLength","GetCompatiblityDescriptorLength method [Microsoft TV Technologies]","GetCompatiblityDescriptorLength method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetCompatiblityDescriptorLength method","IIsdbDownloadContentDescriptor.GetCompatiblityDescriptorLength","IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength","dvbsiparser/IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength","mstv.iisdbdownloadcontentdescriptor_getcompatiblitydescriptorlength"]
old-location: mstv\iisdbdownloadcontentdescriptor_getcompatiblitydescriptorlength.htm
tech.root: mstv
ms.assetid: b8fc770c-aa37-4f97-beb5-6e5747904a6c
ms.date: 12/05/2018
ms.keywords: GetCompatiblityDescriptorLength, GetCompatiblityDescriptorLength method [Microsoft TV Technologies], GetCompatiblityDescriptorLength method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetCompatiblityDescriptorLength method, IIsdbDownloadContentDescriptor.GetCompatiblityDescriptorLength, IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength, dvbsiparser/IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength, mstv.iisdbdownloadcontentdescriptor_getcompatiblitydescriptorlength
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
 - IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength
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
 - IIsdbDownloadContentDescriptor.GetCompatiblityDescriptorLength
---

# IIsdbDownloadContentDescriptor::GetCompatiblityDescriptorLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the length of the compatibility descriptor from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.

## -parameters

### -param pwLength [out]

Receives the length of the compatibility descriptor.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcompatiblitydescriptor">IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor</a>