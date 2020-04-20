---
UID: NF:dvbsiparser.IISDB_BIT.GetTableDescriptorByIndex
title: IISDB_BIT::GetTableDescriptorByIndex (dvbsiparser.h)
description: Returns a descriptor for a specified table in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).helpviewer_keywords: ["GetTableDescriptorByIndex","GetTableDescriptorByIndex method [Microsoft TV Technologies]","GetTableDescriptorByIndex method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetTableDescriptorByIndex method","IISDB_BIT.GetTableDescriptorByIndex","IISDB_BIT::GetTableDescriptorByIndex","dvbsiparser/IISDB_BIT::GetTableDescriptorByIndex","mstv.iisdb_bit_gettabledescriptorbyindex"]
old-location: mstv\iisdb_bit_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: 5c6002b2-61c3-4d0c-87b9-682c3277792c
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IISDB_BIT.GetTableDescriptorByIndex, IISDB_BIT::GetTableDescriptorByIndex, dvbsiparser/IISDB_BIT::GetTableDescriptorByIndex, mstv.iisdb_bit_gettabledescriptorbyindex
ms.topic: method
f1_keywords:
- dvbsiparser/IISDB_BIT.GetTableDescriptorByIndex
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
- IISDB_BIT.GetTableDescriptorByIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_BIT::GetTableDescriptorByIndex


## -description


Returns a descriptor for a specified table
  in an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT).


## -parameters




### -param dwIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a> method to get the number of records in the BIT.



### -param ppDescriptor [out]

Specifies which descriptor to retrieve, indexed from zero.
  Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordcountofdescriptors">IISDB_BIT::GetRecordCountOfDescriptors</a> method
  to get the number of descriptors for a particular record.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">IISDB_BIT::GetCountOfRecords</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordcountofdescriptors">IISDB_BIT::GetRecordCountOfDescriptors</a>
 

 

