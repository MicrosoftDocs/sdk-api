---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordInformationType
title: IISDB_NBIT::GetRecordInformationType
author: windows-sdk-content
description: Gets an information_type field from a record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
old-location: mstv\iisdb_nbit_getrecordinformationtype.htm
tech.root: mstv
ms.assetid: 0f51abc1-d797-4666-b5d5-50560fd2f9f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordInformationType, GetRecordInformationType method [Microsoft TV Technologies], GetRecordInformationType method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordInformationType method, IISDB_NBIT.GetRecordInformationType, IISDB_NBIT::GetRecordInformationType, dvbsiparser/IISDB_NBIT::GetRecordInformationType, mstv.iisdb_nbit_getrecordinformationtype
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
 - IISDB_NBIT.GetRecordInformationType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_NBIT::GetRecordInformationType


## -description


Gets an information_type field from 
  a record in an Integrated Services Digital Broadcasting (ISDB)
  network broadcaster information table (NBIT).
  


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
  Call the <a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a> method to get the number of records in the NBIT.



### -param pbVal [out]

Receives the information_type field. This field can contain any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Undefined

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Information (key ID: none)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Information with service identifier (key ID: service identifier)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
Information with genre (key ID: content_nibble, user_nibble)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x4 - 0xF</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>



<a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a>
 

 

