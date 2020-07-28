---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetLangID
title: IDvbDataBroadcastDescriptor::GetLangID (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) data broadcast descriptor. This language code identifies the language used for the text description field.
helpviewer_keywords: ["GetLangID","GetLangID method [Microsoft TV Technologies]","GetLangID method [Microsoft TV Technologies]","IDvbDataBroadcastDescriptor interface","IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies]","GetLangID method","IDvbDataBroadcastDescriptor.GetLangID","IDvbDataBroadcastDescriptor::GetLangID","dvbsiparser/IDvbDataBroadcastDescriptor::GetLangID","mstv.idvbdatabroadcastdescriptor_getlangid"]
old-location: mstv\idvbdatabroadcastdescriptor_getlangid.htm
tech.root: mstv
ms.assetid: 56fc47d6-042e-48ad-a0b8-39646453a6af
ms.date: 12/05/2018
ms.keywords: GetLangID, GetLangID method [Microsoft TV Technologies], GetLangID method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetLangID method, IDvbDataBroadcastDescriptor.GetLangID, IDvbDataBroadcastDescriptor::GetLangID, dvbsiparser/IDvbDataBroadcastDescriptor::GetLangID, mstv.idvbdatabroadcastdescriptor_getlangid
f1_keywords:
- dvbsiparser/IDvbDataBroadcastDescriptor.GetLangID
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
- IDvbDataBroadcastDescriptor.GetLangID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbDataBroadcastDescriptor::GetLangID


## -description


Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) data broadcast descriptor. This language code
identifies the language used for the text description field. 


## -parameters




### -param pulVal [out]

Receives the language code. For a list of language codes, refer to the <a href="http://www-01.sil.org/iso639-3/codes.asp">ISO 639 Code Tables</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastdescriptor">IDvbDataBroadcastDescriptor</a>
 

 

