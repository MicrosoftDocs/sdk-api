---
UID: NF:dvbsiparser.IISDB_SDT.GetRecordEITUserDefinedFlags
title: IISDB_SDT::GetRecordEITUserDefinedFlags (dvbsiparser.h)
description: Returns the EIT_user_defined_flags field value from a service descriptor in an Integrated Services Digital Broadcasting (ISDB) service description table (SDT).
helpviewer_keywords: ["GetRecordEITUserDefinedFlags","GetRecordEITUserDefinedFlags method [Microsoft TV Technologies]","GetRecordEITUserDefinedFlags method [Microsoft TV Technologies]","IISDB_SDT interface","IISDB_SDT interface [Microsoft TV Technologies]","GetRecordEITUserDefinedFlags method","IISDB_SDT.GetRecordEITUserDefinedFlags","IISDB_SDT::GetRecordEITUserDefinedFlags","dvbsiparser/IISDB_SDT::GetRecordEITUserDefinedFlags","mstv.iisdb_sdt_getrecordeituserdefinedflags"]
old-location: mstv\iisdb_sdt_getrecordeituserdefinedflags.htm
tech.root: mstv
ms.assetid: c67d37e5-f258-45f5-8bc7-c539e3fa5e1a
ms.date: 12/05/2018
ms.keywords: GetRecordEITUserDefinedFlags, GetRecordEITUserDefinedFlags method [Microsoft TV Technologies], GetRecordEITUserDefinedFlags method [Microsoft TV Technologies],IISDB_SDT interface, IISDB_SDT interface [Microsoft TV Technologies],GetRecordEITUserDefinedFlags method, IISDB_SDT.GetRecordEITUserDefinedFlags, IISDB_SDT::GetRecordEITUserDefinedFlags, dvbsiparser/IISDB_SDT::GetRecordEITUserDefinedFlags, mstv.iisdb_sdt_getrecordeituserdefinedflags
f1_keywords:
- dvbsiparser/IISDB_SDT.GetRecordEITUserDefinedFlags
dev_langs:
- c++
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
- IISDB_SDT.GetRecordEITUserDefinedFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_SDT::GetRecordEITUserDefinedFlags


## -description


Returns the EIT_user_defined_flags field value from a service descriptor
  in an Integrated Services Digital Broadcasting (ISDB)
  service description table (SDT). 


## -parameters




### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getcountofrecords">IDVB_SDT::GetCountOfRecords</a>method to get the number of records in the SDT.



### -param pbVal [out]

Receives the EIT_user_defined_flags field value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_sdt-getcountofrecords">IDVB_SDT::GetCountOfRecords</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdt">IISDB_SDT</a>
 

 

