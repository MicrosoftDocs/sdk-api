---
UID: NF:dvbsiparser.IPBDA_EIT.GetRecordEventId
title: IPBDA_EIT::GetRecordEventId
author: windows-sdk-content
description: Receives the unique identifier from an event record in an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbda_eit_getrecordeventid.htm
tech.root: MSTV
ms.assetid: c34ad3ee-f4f9-4088-88ae-1340ea503cf5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRecordEventId, GetRecordEventId method [Microsoft TV Technologies], GetRecordEventId method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetRecordEventId method, IPBDA_EIT.GetRecordEventId, IPBDA_EIT::GetRecordEventId, dvbsiparser/IPBDA_EIT::GetRecordEventId, mstv.ipbda_eit_getrecordeventid
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
 - IPBDA_EIT.GetRecordEventId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IPBDA_EIT.GetRecordEventId
: 
---

# IPBDA_EIT::GetRecordEventId


## -description


Receives the unique identifier from an event record in an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/en-us/library/Dd694799(v=VS.85).aspx">IPBDA_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.



### -param plwVal [out]

Receives the event identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb8cd2cc-e498-43c2-ae1e-3543b4ea3b56">IPBDA_EIT</a>
 

 

