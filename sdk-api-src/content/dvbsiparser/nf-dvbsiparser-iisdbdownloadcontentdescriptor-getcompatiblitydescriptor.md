---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor
title: IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor (dvbsiparser.h)
description: Gets data from the compatibility descriptor in an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The compatibility descriptor specifies a target to be updated by the download.
helpviewer_keywords: ["GetCompatiblityDescriptor","GetCompatiblityDescriptor method [Microsoft TV Technologies]","GetCompatiblityDescriptor method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetCompatiblityDescriptor method","IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor","IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor","dvbsiparser/IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor","mstv.iisdbdownloadcontentdescriptor_getcompatiblitydescriptor"]
old-location: mstv\iisdbdownloadcontentdescriptor_getcompatiblitydescriptor.htm
tech.root: mstv
ms.assetid: 054fe987-49e1-4434-a9b9-6b1030fa2c41
ms.date: 12/05/2018
ms.keywords: GetCompatiblityDescriptor, GetCompatiblityDescriptor method [Microsoft TV Technologies], GetCompatiblityDescriptor method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetCompatiblityDescriptor method, IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor, IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor, dvbsiparser/IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor, mstv.iisdbdownloadcontentdescriptor_getcompatiblitydescriptor
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
 - IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor
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
 - IIsdbDownloadContentDescriptor.GetCompatiblityDescriptor
---

# IIsdbDownloadContentDescriptor::GetCompatiblityDescriptor


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets data from the compatibility descriptor in  an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The compatibility descriptor specifies a target to be updated by the download.

## -parameters

### -param ppbData [out]

Pointer to a buffer that receives the compatibility descriptor. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>