---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetCountOfRecords
title: IDvbServiceListDescriptor::GetCountOfRecords
author: windows-driver-content
description: Gets an indexed count of service records for a Digital Video Broadcast (DVB) service list descriptor.
old-location: mstv\idvbservicelistdescriptor_getcountofrecords.htm
old-project: mstv
ms.assetid: 8a3dd6b9-a7a1-49fd-806d-05c726bbe99e
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbServiceListDescriptor.GetCountOfRecords, IDvbServiceListDescriptor::GetCountOfRecords, dvbsiparser/IDvbServiceListDescriptor::GetCountOfRecords, mstv.idvbservicelistdescriptor_getcountofrecords
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
-	IDvbServiceListDescriptor.GetCountOfRecords
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbServiceListDescriptor::GetCountOfRecords


## -description


Gets an indexed count of service records for a Digital Video Broadcast (DVB) service list descriptor. 


## -parameters




### -param pbVal [out]

Receives the number of service records.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d39595b-0297-473d-9b0f-e038a938a196">IDvbServiceListDescriptor</a>
 

 

