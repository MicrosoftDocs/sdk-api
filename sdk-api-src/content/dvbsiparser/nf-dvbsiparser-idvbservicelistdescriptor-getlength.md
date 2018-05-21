---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetLength
title: IDvbServiceListDescriptor::GetLength
author: windows-driver-content
description: Gets the descriptor_length field value from a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicelistdescriptor_getlength.htm
old-project: mstv
ms.assetid: 06c161ce-b830-4375-8ed6-19403857f433
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbServiceListDescriptor.GetLength, IDvbServiceListDescriptor::GetLength, dvbsiparser/IDvbServiceListDescriptor::GetLength, mstv.idvbservicelistdescriptor_getlength
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
-	IDvbServiceListDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbServiceListDescriptor::GetLength


## -description


Gets the descriptor_length field value from a Digital Video Broadcast (DVB) service descriptor. 


## -parameters




### -param pbVal [out]

Receives the descriptor length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d39595b-0297-473d-9b0f-e038a938a196">IDvbServiceListDescriptor</a>
 

 

