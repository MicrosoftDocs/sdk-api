---
UID: NF:dvbsiparser.IISDB_SDT.GetRecordEITUserDefinedFlags
title: IISDB_SDT::GetRecordEITUserDefinedFlags
author: windows-sdk-content
description: Returns the EIT_user_defined_flags field value from a service descriptor in an Integrated Services Digital Broadcasting (ISDB) service description table (SDT).
old-location: mstv\iisdb_sdt_getrecordeituserdefinedflags.htm
old-project: mstv
ms.assetid: c67d37e5-f258-45f5-8bc7-c539e3fa5e1a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordEITUserDefinedFlags, GetRecordEITUserDefinedFlags method [Microsoft TV Technologies], GetRecordEITUserDefinedFlags method [Microsoft TV Technologies],IISDB_SDT interface, IISDB_SDT interface [Microsoft TV Technologies],GetRecordEITUserDefinedFlags method, IISDB_SDT.GetRecordEITUserDefinedFlags, IISDB_SDT::GetRecordEITUserDefinedFlags, dvbsiparser/IISDB_SDT::GetRecordEITUserDefinedFlags, mstv.iisdb_sdt_getrecordeituserdefinedflags
ms.prod: windows
ms.technology: windows-sdk
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
-	IISDB_SDT.GetRecordEITUserDefinedFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDT::GetRecordEITUserDefinedFlags


## -description



  Returns the EIT_user_defined_flags field value from a service descriptor
  in an Integrated Services Digital Broadcasting (ISDB)
  service description table (SDT). 


## -parameters




### -param dwRecordIndex [in]


  Specifies the record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/9815ba89-d5c2-4d13-8ed1-478953836bc7">IDVB_SDT::GetCountOfRecords</a>
  method to get the number of records in the SDT.



### -param pbVal [out]

Receives the EIT_user_defined_flags field value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9815ba89-d5c2-4d13-8ed1-478953836bc7">IDVB_SDT::GetCountOfRecords</a>



<a href="https://msdn.microsoft.com/a9824eb9-ec12-4a09-ba42-243fe19c0670">IISDB_SDT</a>
 

 

