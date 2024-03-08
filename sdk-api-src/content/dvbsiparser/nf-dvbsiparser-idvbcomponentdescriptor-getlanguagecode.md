---
UID: NF:dvbsiparser.IDvbComponentDescriptor.GetLanguageCode
title: IDvbComponentDescriptor::GetLanguageCode (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) component descriptor.
helpviewer_keywords: ["GetLanguageCode","GetLanguageCode method [Microsoft TV Technologies]","GetLanguageCode method [Microsoft TV Technologies]","IDvbComponentDescriptor interface","IDvbComponentDescriptor interface [Microsoft TV Technologies]","GetLanguageCode method","IDvbComponentDescriptor.GetLanguageCode","IDvbComponentDescriptor::GetLanguageCode","dvbsiparser/IDvbComponentDescriptor::GetLanguageCode","mstv.idvbcomponentdescriptor_getlanguagecode"]
old-location: mstv\idvbcomponentdescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: 9898cd33-db5d-41d3-9e3d-77da2ff38e44
ms.date: 12/05/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IDvbComponentDescriptor interface, IDvbComponentDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IDvbComponentDescriptor.GetLanguageCode, IDvbComponentDescriptor::GetLanguageCode, dvbsiparser/IDvbComponentDescriptor::GetLanguageCode, mstv.idvbcomponentdescriptor_getlanguagecode
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
 - IDvbComponentDescriptor::GetLanguageCode
 - dvbsiparser/IDvbComponentDescriptor::GetLanguageCode
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
 - IDvbComponentDescriptor.GetLanguageCode
---

# IDvbComponentDescriptor::GetLanguageCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) component descriptor.

## -parameters

### -param pszCode

Pointer to the buffer that receives the language code. For a list of language codes, refer to the <a href="http://www.sil.org/ISO639-3/codes.asp">ISO 639 Code Tables</a>. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcomponentdescriptor">IDvbComponentDescriptor</a>