---
UID: NF:dvbsiparser.IPBDA_EIT.GetRecordStartTime
title: IPBDA_EIT::GetRecordStartTime
author: windows-sdk-content
description: Gets the start time from an event record in an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbda_eit_getrecordstarttime.htm
old-project: mstv
ms.assetid: 7022ac7c-b0ea-4ca1-931f-b09906f67df7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordStartTime, GetRecordStartTime method [Microsoft TV Technologies], GetRecordStartTime method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetRecordStartTime method, IPBDA_EIT.GetRecordStartTime, IPBDA_EIT::GetRecordStartTime, dvbsiparser/IPBDA_EIT::GetRecordStartTime, mstv.ipbda_eit_getrecordstarttime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.redist: 
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_EIT.GetRecordStartTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDA_EIT::GetRecordStartTime


## -description


 Gets the start time from an event record in an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/en-us/library/Dd694799(v=VS.85).aspx">IPBDA_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.



### -param pmdtVal [out]

Pointer to an <a href="https://msdn.microsoft.com/586269c5-3415-4a5c-8c8f-b405a7bc3f56">MPEG_DATE_AND_TIME</a> structure that receives the start time from the event record.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb8cd2cc-e498-43c2-ae1e-3543b4ea3b56">IPBDA_EIT</a>
 

 

