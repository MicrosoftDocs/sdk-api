---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetRecordLangId
title: IDvbSubtitlingDescriptor::GetRecordLangId (dvbsiparser.h)

description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) subtitling descriptor. This code identifies the language used for subtitles.
old-location: mstv\idvbsubtitlingdescriptor_getrecordlangid.htm
tech.root: mstv
ms.assetid: 03a6a71f-ccec-4e4f-a24c-2ac81dd1a0ba

ms.date: 12/05/2018
ms.keywords: GetRecordLangId, GetRecordLangId method [Microsoft TV Technologies], GetRecordLangId method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetRecordLangId method, IDvbSubtitlingDescriptor.GetRecordLangId, IDvbSubtitlingDescriptor::GetRecordLangId, dvbsiparser/IDvbSubtitlingDescriptor::GetRecordLangId, mstv.idvbsubtitlingdescriptor_getrecordlangid
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDvbSubtitlingDescriptor.GetRecordLangId"
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
 - IDvbSubtitlingDescriptor.GetRecordLangId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbSubtitlingDescriptor::GetRecordLangId


## -description


Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) subtitling descriptor. This code
identifies the language used for subtitles.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>



### -param pulVal [out]

Pointer to a buffer that receives the language code. For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">this document</a>. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsubtitlingdescriptor">IDvbSubtitlingDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsubtitlingdescriptor-getcountofrecords">IDvbSubtitlingDescriptor::GetCountOfRecords</a>
 

 

