---
UID: NF:dvbsiparser.IISDB_BIT.GetTableDescriptorByTag
title: IISDB_BIT::GetTableDescriptorByTag (dvbsiparser.h)
author: windows-sdk-content
description: Searches a subtable in for an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_gettabledescriptorbytag.htm
tech.root: mstv
ms.assetid: ef54b6bc-7150-4246-8058-4e57f25c2ad3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByTag, GetTableDescriptorByTag method [Microsoft TV Technologies], GetTableDescriptorByTag method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetTableDescriptorByTag method, IISDB_BIT.GetTableDescriptorByTag, IISDB_BIT::GetTableDescriptorByTag, dvbsiparser/IISDB_BIT::GetTableDescriptorByTag, mstv.iisdb_bit_gettabledescriptorbytag
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
 - IISDB_BIT.GetTableDescriptorByTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_BIT::GetTableDescriptorByTag


## -description


Searches a subtable in
  for an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT). 


## -parameters




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

Address of a variable that receives an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor
  </a>interface pointer. Use this interface to retrieve the information
  in the descriptor. The caller must release the interface.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>
 

 

