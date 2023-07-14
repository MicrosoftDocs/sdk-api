---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetLanguageCode
title: IIsdbDataContentDescriptor::GetLanguageCode (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) data content descriptor.
helpviewer_keywords: ["GetLanguageCode","GetLanguageCode method [Microsoft TV Technologies]","GetLanguageCode method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetLanguageCode method","IIsdbDataContentDescriptor.GetLanguageCode","IIsdbDataContentDescriptor::GetLanguageCode","dvbsiparser/IIsdbDataContentDescriptor::GetLanguageCode","mstv.iisdbdatacontentdescriptor_getlanguagecode"]
old-location: mstv\iisdbdatacontentdescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: bbf89870-e258-43d8-8312-edc53998e51a
ms.date: 12/05/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IIsdbDataContentDescriptor.GetLanguageCode, IIsdbDataContentDescriptor::GetLanguageCode, dvbsiparser/IIsdbDataContentDescriptor::GetLanguageCode, mstv.iisdbdatacontentdescriptor_getlanguagecode
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
 - IIsdbDataContentDescriptor::GetLanguageCode
 - dvbsiparser/IIsdbDataContentDescriptor::GetLanguageCode
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
 - IIsdbDataContentDescriptor.GetLanguageCode
---

# IIsdbDataContentDescriptor::GetLanguageCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) data content descriptor.

## -parameters

### -param pszCode

Pointer to the buffer that receives the language code. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>