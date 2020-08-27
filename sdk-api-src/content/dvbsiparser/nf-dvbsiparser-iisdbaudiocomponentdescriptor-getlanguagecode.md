---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetLanguageCode
title: IIsdbAudioComponentDescriptor::GetLanguageCode (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. If the stream uses ES multilingual mode, this method returns the first language code.
helpviewer_keywords: ["GetLanguageCode","GetLanguageCode method [Microsoft TV Technologies]","GetLanguageCode method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetLanguageCode method","IIsdbAudioComponentDescriptor.GetLanguageCode","IIsdbAudioComponentDescriptor::GetLanguageCode","dvbsiparser/IIsdbAudioComponentDescriptor::GetLanguageCode","mstv.iisdbaudiocomponentdescriptor_getlanguagecode"]
old-location: mstv\iisdbaudiocomponentdescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: 7f44f9c6-7eb6-4c4d-b25b-b2a95dcaa658
ms.date: 12/05/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, IIsdbAudioComponentDescriptor.GetLanguageCode, IIsdbAudioComponentDescriptor::GetLanguageCode, dvbsiparser/IIsdbAudioComponentDescriptor::GetLanguageCode, mstv.iisdbaudiocomponentdescriptor_getlanguagecode
f1_keywords:
- dvbsiparser/IIsdbAudioComponentDescriptor.GetLanguageCode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbAudioComponentDescriptor.GetLanguageCode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor::GetLanguageCode


## -description


Gets the three-character ISO 639 language code from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. If the stream uses ES multilingual mode, this method returns the first language code.


## -parameters




### -param pszCode

Pointer to the buffer that receives the language code.  For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">ISO 639 Code Tables</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
 

 

