---
UID: NF:dvbsiparser.IISDB_BIT.GetTableDescriptorByIndex
title: IISDB_BIT::GetTableDescriptorByIndex
author: windows-sdk-content
description: Returns a descriptor for a specified table in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_gettabledescriptorbyindex.htm
tech.root: MSTV
ms.assetid: 5c6002b2-61c3-4d0c-87b9-682c3277792c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IISDB_BIT.GetTableDescriptorByIndex, IISDB_BIT::GetTableDescriptorByIndex, dvbsiparser/IISDB_BIT::GetTableDescriptorByIndex, mstv.iisdb_bit_gettabledescriptorbyindex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
  Call the <a href="https://msdn.microsoft.com/3f36c03a-462e-479a-ad8c-5322377dbca0">IISDB_BIT::GetCountOfRecords</a> method to get the number of records in the BIT.



### -param ppDescriptor [out]

Specifies which descriptor to retrieve, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/08df6f74-dbeb-4d32-8b0f-4ec88d35ff36">IISDB_BIT::GetRecordCountOfDescriptors</a> method
  to get the number of descriptors for a particular record.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>



<a href="https://msdn.microsoft.com/3f36c03a-462e-479a-ad8c-5322377dbca0">IISDB_BIT::GetCountOfRecords</a>



<a href="https://msdn.microsoft.com/08df6f74-dbeb-4d32-8b0f-4ec88d35ff36">IISDB_BIT::GetRecordCountOfDescriptors</a>
 

 

