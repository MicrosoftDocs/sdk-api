---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetComponentTag
title: IIsdbDownloadContentDescriptor::GetComponentTag (dvbsiparser.h)
description: Gets the tag that identifies a stream component from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. This tag also identifies the stream in the program map table (PMT).helpviewer_keywords: ["GetComponentTag","GetComponentTag method [Microsoft TV Technologies]","GetComponentTag method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetComponentTag method","IIsdbDownloadContentDescriptor.GetComponentTag","IIsdbDownloadContentDescriptor::GetComponentTag","dvbsiparser/IIsdbDownloadContentDescriptor::GetComponentTag","mstv.iisdbdownloadcontentdescriptor_getcomponenttag"]
old-location: mstv\iisdbdownloadcontentdescriptor_getcomponenttag.htm
tech.root: mstv
ms.assetid: d4ba2fbd-4349-48e3-81dd-622442409060
ms.date: 12/05/2018
ms.keywords: GetComponentTag, GetComponentTag method [Microsoft TV Technologies], GetComponentTag method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetComponentTag method, IIsdbDownloadContentDescriptor.GetComponentTag, IIsdbDownloadContentDescriptor::GetComponentTag, dvbsiparser/IIsdbDownloadContentDescriptor::GetComponentTag, mstv.iisdbdownloadcontentdescriptor_getcomponenttag
f1_keywords:
- dvbsiparser/IIsdbDownloadContentDescriptor.GetComponentTag
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbDownloadContentDescriptor.GetComponentTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDownloadContentDescriptor::GetComponentTag


## -description


Gets the tag that identifies  a stream component from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. This tag also identifies the stream in the program map table (PMT).


## -parameters




### -param pbVal [out]

Receives the component tag.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>
 

 

