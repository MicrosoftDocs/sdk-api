---
UID: NF:dvbsiparser.IISDB_LDT.GetRecordDescriptorByIndex
title: IISDB_LDT::GetRecordDescriptorByIndex
author: windows-driver-content
description: Returns a descriptor for a specified record in an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
old-location: mstv\iisdb_ldt_getrecorddescriptorbyindex.htm
old-project: mstv
ms.assetid: a551794a-6051-4c8e-9d44-5938974a6df4
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IISDB_LDT.GetRecordDescriptorByIndex, IISDB_LDT::GetRecordDescriptorByIndex, dvbsiparser/IISDB_LDT::GetRecordDescriptorByIndex, mstv.iisdb_ldt_getrecorddescriptorbyindex
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
-	IISDB_LDT.GetRecordDescriptorByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_LDT::GetRecordDescriptorByIndex


## -description



  Returns a descriptor for a specified record
  in an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT). 



## -parameters




### -param dwRecordIndex [in]


  Specifies the record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/da91deea-527c-4458-9db5-ae500cee19bb">IISDB_LDT::GetCountOfRecords</a> method to get the number of records in the LDT.



### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero.
Call the <a href="https://msdn.microsoft.com/1352eec0-fed2-4d14-81f2-c73b8d34a264">IISDB_LDT::GetRecordCountOfDescriptors</a> method 
to get the number of descriptors for a particular record.


### -param ppDescriptor [out]

Pointer to the <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a>
interface for the object that contains the LDT. Use this interface to retrieve the information in the descriptor. 
The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a>



<a href="https://msdn.microsoft.com/4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3">IISDB_LDT</a>



<a href="https://msdn.microsoft.com/da91deea-527c-4458-9db5-ae500cee19bb">IISDB_LDT::GetCountOfRecords</a>



<a href="https://msdn.microsoft.com/1352eec0-fed2-4d14-81f2-c73b8d34a264">IISDB_LDT::GetRecordCountOfDescriptors</a>
 

 

