---
UID: NF:atscpsipparser.IServiceLocationDescriptor.GetElementLanguageCode
title: IServiceLocationDescriptor::GetElementLanguageCode (atscpsipparser.h)
description: Gets the three-character ISO 639 language code for an Advanced Television Systems Committee (ATSC) service location descriptor.
helpviewer_keywords: ["GetElementLanguageCode","GetElementLanguageCode method [Microsoft TV Technologies]","GetElementLanguageCode method [Microsoft TV Technologies]","IServiceLocationDescriptor interface","IServiceLocationDescriptor interface [Microsoft TV Technologies]","GetElementLanguageCode method","IServiceLocationDescriptor.GetElementLanguageCode","IServiceLocationDescriptor::GetElementLanguageCode","atscpsipparser/IServiceLocationDescriptor::GetElementLanguageCode","mstv.iservicelocationdescriptor_getelementlanguagecode"]
old-location: mstv\iservicelocationdescriptor_getelementlanguagecode.htm
tech.root: mstv
ms.assetid: 8ffc0c58-1305-49bf-bdbd-efb18805516f
ms.date: 12/05/2018
ms.keywords: GetElementLanguageCode, GetElementLanguageCode method [Microsoft TV Technologies], GetElementLanguageCode method [Microsoft TV Technologies],IServiceLocationDescriptor interface, IServiceLocationDescriptor interface [Microsoft TV Technologies],GetElementLanguageCode method, IServiceLocationDescriptor.GetElementLanguageCode, IServiceLocationDescriptor::GetElementLanguageCode, atscpsipparser/IServiceLocationDescriptor::GetElementLanguageCode, mstv.iservicelocationdescriptor_getelementlanguagecode
req.header: atscpsipparser.h
req.include-header: Atscpsipparser.idl
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
 - IServiceLocationDescriptor::GetElementLanguageCode
 - atscpsipparser/IServiceLocationDescriptor::GetElementLanguageCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IServiceLocationDescriptor.GetElementLanguageCode
---

# IServiceLocationDescriptor::GetElementLanguageCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the three-character ISO 639 language code  for an Advanced Television Systems Committee (ATSC) service location descriptor.

## -parameters

### -param bIndex [in]

Specifies the elementary stream,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iservicelocationdescriptor-getnumberofelements">IServiceLocationDescriptor::GetNumberOfElements</a> method to get the number of elementary streams in the descriptor.

### -param LangCode [out]

Pointer to a buffer that receives the language code. For a list of language codes, refer to <a href="http://www-01.sil.org/iso639-3/codes.asp">ISO 639 Code Tables</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iservicelocationdescriptor">IServiceLocationDescriptor</a>