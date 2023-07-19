---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetLanguageCode
title: IDvbExtendedEventDescriptor::GetLanguageCode (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetLanguageCode","GetLanguageCode method [Microsoft TV Technologies]","GetLanguageCode method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetLanguageCode method","IDvbExtendedEventDescriptor.GetLanguageCode","IDvbExtendedEventDescriptor::GetLanguageCode","dvbsiparser/IDvbExtendedEventDescriptor::GetLanguageCode","mstv.idvbextendedeventdescriptor_getlanguagecode"]
old-location: mstv\idvbextendedeventdescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: f63b7fa9-969e-43d4-95f3-445d6265f445
ms.date: 12/05/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IDvbExtendedEventDescriptor.GetLanguageCode, IDvbExtendedEventDescriptor::GetLanguageCode, dvbsiparser/IDvbExtendedEventDescriptor::GetLanguageCode, mstv.idvbextendedeventdescriptor_getlanguagecode
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
 - IDvbExtendedEventDescriptor::GetLanguageCode
 - dvbsiparser/IDvbExtendedEventDescriptor::GetLanguageCode
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
 - IDvbExtendedEventDescriptor.GetLanguageCode
---

# IDvbExtendedEventDescriptor::GetLanguageCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) extended event descriptor.

## -parameters

### -param pszCode

Pointer to the buffer that receives the language code. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>