---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetText
title: IDvbDataBroadcastDescriptor::GetText
author: windows-driver-content
description: Gets the text that describes the data from a Digital Video Broadcast (DVB) data broadcast descriptor.
old-location: mstv\idvbdatabroadcastdescriptor_gettext.htm
old-project: mstv
ms.assetid: 3b25a5fa-5829-4c7f-8858-59fdddccdc65
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetText, GetText method [Microsoft TV Technologies], GetText method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetText method, IDvbDataBroadcastDescriptor.GetText, IDvbDataBroadcastDescriptor::GetText, dvbsiparser/IDvbDataBroadcastDescriptor::GetText, mstv.idvbdatabroadcastdescriptor_gettext
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbDataBroadcastDescriptor.GetText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbDataBroadcastDescriptor::GetText


## -description


Gets the text that describes the data 
from a Digital Video Broadcast (DVB) data broadcast descriptor. 


## -parameters




### -param pbLen [in, out]

Specifies or receives the length of the
description, in bytes.


### -param pbVal [out]

Receives the description text.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b1d2711-e5ad-4d4c-bc8f-e199bcd75799">IDvbDataBroadcastDescriptor</a>
 

 

