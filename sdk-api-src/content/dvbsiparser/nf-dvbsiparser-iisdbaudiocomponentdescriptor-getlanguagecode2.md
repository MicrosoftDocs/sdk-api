---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetLanguageCode2
title: IIsdbAudioComponentDescriptor::GetLanguageCode2 (dvbsiparser.h)
description: In ES multilingual mode, gets the second three-character ISO 639 language code from an ISDB audio component descriptor.
helpviewer_keywords: ["GetLanguageCode2","GetLanguageCode2 method [Microsoft TV Technologies]","GetLanguageCode2 method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetLanguageCode2 method","IIsdbAudioComponentDescriptor.GetLanguageCode2","IIsdbAudioComponentDescriptor::GetLanguageCode2","dvbsiparser/IIsdbAudioComponentDescriptor::GetLanguageCode2","mstv.iisdbaudiocomponentdescriptor_getlanguagecode2"]
old-location: mstv\iisdbaudiocomponentdescriptor_getlanguagecode2.htm
tech.root: mstv
ms.assetid: 3016264e-c952-4243-acd2-a075c89e8c2b
ms.date: 12/05/2018
ms.keywords: GetLanguageCode2, GetLanguageCode2 method [Microsoft TV Technologies], GetLanguageCode2 method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetLanguageCode2 method, IIsdbAudioComponentDescriptor.GetLanguageCode2, IIsdbAudioComponentDescriptor::GetLanguageCode2, dvbsiparser/IIsdbAudioComponentDescriptor::GetLanguageCode2, mstv.iisdbaudiocomponentdescriptor_getlanguagecode2
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbAudioComponentDescriptor::GetLanguageCode2
 - dvbsiparser/IIsdbAudioComponentDescriptor::GetLanguageCode2
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
 - IIsdbAudioComponentDescriptor.GetLanguageCode2
---

# IIsdbAudioComponentDescriptor::GetLanguageCode2


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

In ES multilingual mode, gets the second  three-character ISO 639 language code from an ISDB audio component descriptor.

## -parameters

### -param pszCode

Pointer to the buffer that receives the language code.  For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">ISO 639 Code Tables</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>