---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordDescriptorByTag
title: IISDB_NBIT::GetRecordDescriptorByTag
author: windows-sdk-content
description: Gets a descriptor from a record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT) by using the standard tag for the descriptor.
old-location: mstv\iisdb_nbit_getrecorddescriptorbytag.htm
old-project: mstv
ms.assetid: baec7c6a-67a7-4081-96ee-3cb35a72ff4e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IISDB_NBIT.GetRecordDescriptorByTag, IISDB_NBIT::GetRecordDescriptorByTag, dvbsiparser/IISDB_NBIT::GetRecordDescriptorByTag, mstv.iisdb_nbit_getrecorddescriptorbytag
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_NBIT.GetRecordDescriptorByTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_NBIT::GetRecordDescriptorByTag


## -description


Gets a descriptor from a record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT)
  by using the standard tag for the descriptor.
  


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a> method to get the number of records in the NBIT.


### -param bTag [in]

Specifies the descriptor tag for which to search.


### -param pdwCookie [in, out]

Receives 
the start position in the descriptor list. This parameter is optional. 
If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the first descriptor in the list. Otherwise, the search starts from the position given in <i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i> parameter contains the position of the next matching descriptor, if any. You can use this parameter to iterate through the descriptor list, 
looking for every instance of a particular descriptor tag.


### -param ppDescriptor [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> interface pointer. 
Use this interface to retrieve the information 
in the descriptor. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a>



<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>



<a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a>
 

 

