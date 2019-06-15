---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetRecordLangId
title: IDvbTeletextDescriptor::GetRecordLangId (dvbsiparser.h)
author: windows-sdk-content
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) teletext descriptor.
old-location: mstv\idvbteletextdescriptor_getrecordlangid.htm
tech.root: mstv
ms.assetid: cce0fd15-5098-4871-baab-e40b6cae39b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordLangId, GetRecordLangId method [Microsoft TV Technologies], GetRecordLangId method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetRecordLangId method, IDvbTeletextDescriptor.GetRecordLangId, IDvbTeletextDescriptor::GetRecordLangId, dvbsiparser/IDvbTeletextDescriptor::GetRecordLangId, mstv.idvbteletextdescriptor_getrecordlangid
ms.topic: method
f1_keywords: ["dvbsiparser/IDvbTeletextDescriptor.GetRecordLangId"]
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
 - IDvbTeletextDescriptor.GetRecordLangId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbTeletextDescriptor::GetRecordLangId


## -description


Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB)
  teletext descriptor. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, 
  call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getcountofrecords">IDvbTeletextDescriptor::GetCountOfRecords</a>.



### -param pulVal [out]

Pointer to a 24-bit buffer that receives the language code.  For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">this document</a>. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbteletextdescriptor">IDvbTeletextDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbteletextdescriptor-getcountofrecords">IDvbTeletextDescriptor::GetCountOfRecords</a>
 

 

