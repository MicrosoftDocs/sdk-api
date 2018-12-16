---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetRecordLangId
title: IDvbSubtitlingDescriptor::GetRecordLangId
author: windows-sdk-content
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) subtitling descriptor. This code identifies the language used for subtitles.
old-location: mstv\idvbsubtitlingdescriptor_getrecordlangid.htm
tech.root: mstv
ms.assetid: 03a6a71f-ccec-4e4f-a24c-2ac81dd1a0ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordLangId, GetRecordLangId method [Microsoft TV Technologies], GetRecordLangId method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetRecordLangId method, IDvbSubtitlingDescriptor.GetRecordLangId, IDvbSubtitlingDescriptor::GetRecordLangId, dvbsiparser/IDvbSubtitlingDescriptor::GetRecordLangId, mstv.idvbsubtitlingdescriptor_getrecordlangid
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSubtitlingDescriptor::GetRecordLangId


## -description


Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) subtitling descriptor. This code
identifies the language used for subtitles.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/8cc25b63-de43-4f8d-af19-c3bb8c389a55">IDvbSubtitlingDescriptor::GetCountOfRecords</a>



### -param pulVal [out]

Pointer to a buffer that receives the language code. For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">this document</a>. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7308e8a9-6e16-4719-b87e-9445499f499c">IDvbSubtitlingDescriptor</a>



<a href="https://msdn.microsoft.com/8cc25b63-de43-4f8d-af19-c3bb8c389a55">IDvbSubtitlingDescriptor::GetCountOfRecords</a>
 

 

