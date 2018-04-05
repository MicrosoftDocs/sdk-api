---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetTextLength
title: IDvbDataBroadcastDescriptor::GetTextLength method
author: windows-driver-content
description: Gets length of the text description, in bytes, from a Digital Video Broadcast (DVB) data broadcast descriptor.
old-location: mstv\idvbdatabroadcastdescriptor_gettextlength.htm
old-project: mstv
ms.assetid: a5ae91ff-d984-4955-aa1c-d166fb491d79
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetTextLength method [Microsoft TV Technologies], GetTextLength method [Microsoft TV Technologies], IDvbDataBroadcastDescriptor interface, GetTextLength,IDvbDataBroadcastDescriptor.GetTextLength, IDvbDataBroadcastDescriptor, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies], GetTextLength method, IDvbDataBroadcastDescriptor::GetTextLength, dvbsiparser/IDvbDataBroadcastDescriptor::GetTextLength, mstv.idvbdatabroadcastdescriptor_gettextlength
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
-	IDvbDataBroadcastDescriptor.GetTextLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbDataBroadcastDescriptor::GetTextLength method


## -description


Gets length of the text description, in bytes, from a Digital Video Broadcast (DVB)
data broadcast descriptor. 


## -parameters




### -param pbVal [out]

Receives the text description length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b1d2711-e5ad-4d4c-bc8f-e199bcd75799">IDvbDataBroadcastDescriptor</a>
 

 

