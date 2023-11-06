---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetTextLanguageCode
title: IIsdbDownloadContentDescriptor::GetTextLanguageCode (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
helpviewer_keywords: ["GetTextLanguageCode","GetTextLanguageCode method [Microsoft TV Technologies]","GetTextLanguageCode method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetTextLanguageCode method","IIsdbDownloadContentDescriptor.GetTextLanguageCode","IIsdbDownloadContentDescriptor::GetTextLanguageCode","dvbsiparser/IIsdbDownloadContentDescriptor::GetTextLanguageCode","mstv.iisdbdownloadcontentdescriptor_gettextlanguagecode"]
old-location: mstv\iisdbdownloadcontentdescriptor_gettextlanguagecode.htm
tech.root: mstv
ms.assetid: 023e2b6f-0f38-4550-a839-29c254970219
ms.date: 12/05/2018
ms.keywords: GetTextLanguageCode, GetTextLanguageCode method [Microsoft TV Technologies], GetTextLanguageCode method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetTextLanguageCode method, IIsdbDownloadContentDescriptor.GetTextLanguageCode, IIsdbDownloadContentDescriptor::GetTextLanguageCode, dvbsiparser/IIsdbDownloadContentDescriptor::GetTextLanguageCode, mstv.iisdbdownloadcontentdescriptor_gettextlanguagecode
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
 - IIsdbDownloadContentDescriptor::GetTextLanguageCode
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetTextLanguageCode
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
 - IIsdbDownloadContentDescriptor.GetTextLanguageCode
---

# IIsdbDownloadContentDescriptor::GetTextLanguageCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.

## -parameters

### -param szCode

Receives the language code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>