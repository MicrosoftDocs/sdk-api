---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetSelectorLength
title: IDvbDataBroadcastDescriptor::GetSelectorLength (dvbsiparser.h)
author: windows-sdk-content
description: Gets the length of the selector in a DVB data broadcast descriptor, in bytes. The selector is defined by the data broadcast specification for the network.
old-location: mstv\idvbdatabroadcastdescriptor_getselectorlength.htm
tech.root: mstv
ms.assetid: fc1d25be-6f33-4281-a75c-74c7331ab6ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSelectorLength, GetSelectorLength method [Microsoft TV Technologies], GetSelectorLength method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetSelectorLength method, IDvbDataBroadcastDescriptor.GetSelectorLength, IDvbDataBroadcastDescriptor::GetSelectorLength, dvbsiparser/IDvbDataBroadcastDescriptor::GetSelectorLength, mstv.idvbdatabroadcastdescriptor_getselectorlength
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDvbDataBroadcastDescriptor.GetSelectorLength"
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
 - IDvbDataBroadcastDescriptor.GetSelectorLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbDataBroadcastDescriptor::GetSelectorLength


## -description


Gets the length of the selector in a DVB data broadcast descriptor, in bytes. The selector is defined by the 
data broadcast specification for the network.


## -parameters




### -param pbVal [out]

Receives the selector length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastdescriptor">IDvbDataBroadcastDescriptor</a>
 

 

