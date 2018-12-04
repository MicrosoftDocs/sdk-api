---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetLangID
title: IDvbDataBroadcastDescriptor::GetLangID
author: windows-sdk-content
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) data broadcast descriptor. This language code identifies the language used for the text description field.
old-location: mstv\idvbdatabroadcastdescriptor_getlangid.htm
tech.root: mstv
ms.assetid: 56fc47d6-042e-48ad-a0b8-39646453a6af
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLangID, GetLangID method [Microsoft TV Technologies], GetLangID method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetLangID method, IDvbDataBroadcastDescriptor.GetLangID, IDvbDataBroadcastDescriptor::GetLangID, dvbsiparser/IDvbDataBroadcastDescriptor::GetLangID, mstv.idvbdatabroadcastdescriptor_getlangid
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDvbDataBroadcastDescriptor.GetLangID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbDataBroadcastDescriptor::GetLangID


## -description


Gets the three-character ISO 639 language code from
a Digital Video Broadcast (DVB) data broadcast descriptor. This language code
identifies the language used for the text description field. 


## -parameters




### -param pulVal [out]

Receives the language code. For a list of language codes, refer to the <a href=" http://go.microsoft.com/fwlink?linkID=161422">ISO 639 Code Tables</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b1d2711-e5ad-4d4c-bc8f-e199bcd75799">IDvbDataBroadcastDescriptor</a>
 

 

