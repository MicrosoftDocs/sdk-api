---
UID: NF:dvbsiparser.IISDB_LDT.GetRecordDescriptorByTag
title: IISDB_LDT::GetRecordDescriptorByTag
author: windows-sdk-content
description: Searches a record in an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT) for a specific descriptor tag.
old-location: mstv\iisdb_ldt_getrecorddescriptorbytag.htm
tech.root: MSTV
ms.assetid: 6d1fc08c-9c5b-4361-a144-d8b423250c51
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IISDB_LDT.GetRecordDescriptorByTag, IISDB_LDT::GetRecordDescriptorByTag, dvbsiparser/IISDB_LDT::GetRecordDescriptorByTag, mstv.iisdb_ldt_getrecorddescriptorbytag
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
 - IISDB_LDT.GetRecordDescriptorByTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_LDT::GetRecordDescriptorByTag


## -description


Searches a record in
  an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT) for a specific descriptor tag. 


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/da91deea-527c-4458-9db5-ae500cee19bb">IISDB_LDT::GetCountOfRecords</a> method to get the number of records in the LDT.



### -param bTag [in]

Specifies the descriptor tag for which to search.


### -param pdwCookie [in, out]

Pointer to a variable that specifies the start position
  in the descriptor list. This parameter is optional.
  If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the
  first descriptor in the list. Otherwise, the search starts from
  the position given in <i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i>parameter contains the position of the next matching descriptor,
  if any. You can use this parameter to iterate through the descriptor list,
  looking for every instance of a particular descriptor tag.



### -param ppDescriptor [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a>interface of the object that contains the LDT. Use this interface to retrieve the information
  in the descriptor. The caller must release the interface.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a>



<a href="https://msdn.microsoft.com/4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3">IISDB_LDT</a>



<a href="https://msdn.microsoft.com/da91deea-527c-4458-9db5-ae500cee19bb">IISDB_LDT::GetCountOfRecords</a>
 

 

