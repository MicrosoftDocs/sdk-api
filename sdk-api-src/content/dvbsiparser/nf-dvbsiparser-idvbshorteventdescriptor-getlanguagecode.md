---
UID: NF:dvbsiparser.IDvbShortEventDescriptor.GetLanguageCode
title: IDvbShortEventDescriptor::GetLanguageCode (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) short event descriptor.
helpviewer_keywords: ["GetLanguageCode","GetLanguageCode method [Microsoft TV Technologies]","GetLanguageCode method [Microsoft TV Technologies]","IDvbShortEventDescriptor interface","IDvbShortEventDescriptor interface [Microsoft TV Technologies]","GetLanguageCode method","IDvbShortEventDescriptor.GetLanguageCode","IDvbShortEventDescriptor::GetLanguageCode","dvbsiparser/IDvbShortEventDescriptor::GetLanguageCode","mstv.idvbshorteventdescriptor_getlanguagecode"]
old-location: mstv\idvbshorteventdescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: c531ae74-586f-4191-9b77-5f5837e551c4
ms.date: 12/05/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IDvbShortEventDescriptor interface, IDvbShortEventDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IDvbShortEventDescriptor.GetLanguageCode, IDvbShortEventDescriptor::GetLanguageCode, dvbsiparser/IDvbShortEventDescriptor::GetLanguageCode, mstv.idvbshorteventdescriptor_getlanguagecode
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
 - IDvbShortEventDescriptor::GetLanguageCode
 - dvbsiparser/IDvbShortEventDescriptor::GetLanguageCode
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
 - IDvbShortEventDescriptor.GetLanguageCode
---

# IDvbShortEventDescriptor::GetLanguageCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) short event descriptor.

## -parameters

### -param pszCode

Receives the language code. For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">this document</a>. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbshorteventdescriptor">IDvbShortEventDescriptor</a>