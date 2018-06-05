---
UID: NF:dvbsiparser.IISDB_BIT.GetRecordDescriptorByTag
title: IISDB_BIT::GetRecordDescriptorByTag
author: windows-sdk-content
description: Searches a record in an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_getrecorddescriptorbytag.htm
old-project: mstv
ms.assetid: 9e22da6e-1721-46c5-9a98-7d21edaa6d14
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IISDB_BIT.GetRecordDescriptorByTag, IISDB_BIT::GetRecordDescriptorByTag, dvbsiparser/IISDB_BIT::GetRecordDescriptorByTag, mstv.iisdb_bit_getrecorddescriptorbytag
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_BIT.GetRecordDescriptorByTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_BIT::GetRecordDescriptorByTag


## -description



  Searches a record in
  an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
  


## -parameters




### -param dwRecordIndex [in]


  Specifies the record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/3f36c03a-462e-479a-ad8c-5322377dbca0">IISDB_BIT::GetCountOfRecords</a> method to get the number of records in the BIT.



### -param bTag [in]

Specifies the descriptor tag for which to search.


### -param pdwCookie [in, out]


  Pointer to a variable that specifies the start position
  in the descriptor list. This parameter is optional.
  If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the
  first descriptor in the list. Otherwise, the search starts from
  the position given in <i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i>
  parameter contains the position of the next matching descriptor,
  if any. You can use this parameter to iterate through the descriptor list,
  looking for every instance of a particular descriptor tag.



### -param ppDescriptor [out]


  Address of a variable that receives an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor
  </a> interface pointer. Use this interface to retrieve the information
  in the descriptor. The caller must release the interface.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor
  </a>



<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>



<a href="https://msdn.microsoft.com/3f36c03a-462e-479a-ad8c-5322377dbca0">IISDB_BIT::GetCountOfRecords</a>
 

 

