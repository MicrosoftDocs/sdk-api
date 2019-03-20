---
UID: NF:dvbsiparser.IPBDA_EIT.GetRecordCountOfDescriptors
title: IPBDA_EIT::GetRecordCountOfDescriptors (dvbsiparser.h)
author: windows-sdk-content
description: Gets the number of event records from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbda_eit_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: c491b2d0-6426-4a76-b3a1-4477fdf1779c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IPBDA_EIT.GetRecordCountOfDescriptors, IPBDA_EIT::GetRecordCountOfDescriptors, dvbsiparser/IPBDA_EIT::GetRecordCountOfDescriptors, mstv.ipbda_eit_getrecordcountofdescriptors
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
 - IPBDA_EIT.GetRecordCountOfDescriptors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPBDA_EIT::GetRecordCountOfDescriptors


## -description


Gets the number of event records from an  event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/7f09421d-ae19-4c8e-93a2-31fa8697742a">IPBDA_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.



### -param pdwVal [out]

Receives the number of descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb8cd2cc-e498-43c2-ae1e-3543b4ea3b56">IPBDA_EIT</a>
 

 

