---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordDescriptionBodyLocation
title: IISDB_NBIT::GetRecordDescriptionBodyLocation
author: windows-driver-content
description: Receives the value of the description_body_location field from a record in an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
old-location: mstv\iisdb_nbit_getrecorddescriptionbodylocation.htm
old-project: mstv
ms.assetid: bb022e1f-6f46-4cdc-8f43-4c4475acf621
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetRecordDescriptionBodyLocation, GetRecordDescriptionBodyLocation method [Microsoft TV Technologies], GetRecordDescriptionBodyLocation method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordDescriptionBodyLocation method, IISDB_NBIT.GetRecordDescriptionBodyLocation, IISDB_NBIT::GetRecordDescriptionBodyLocation, dvbsiparser/IISDB_NBIT::GetRecordDescriptionBodyLocation, mstv.iisdb_nbit_getrecorddescriptionbodylocation
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
-	IISDB_NBIT.GetRecordDescriptionBodyLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_NBIT::GetRecordDescriptionBodyLocation


## -description


Receives the value of the description_body_location field
  from a record in an Integrated Services Digital Broadcasting (ISDB)
  network broadcaster information table (NBIT).
  This field value indicates the location of the table where the information contents are described.


## -parameters




### -param dwRecordIndex [in]

Index of a record containing descriptors in the NBIT.


### -param pbVal [out]

Receives a 2-bit code that indicates the location of the descriptors. This can be any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>00</dt>
</dl>
</td>
<td width="60%">
Undefined

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>01</dt>
</dl>
</td>
<td width="60%">
Detailed information is provided in the actual transport stream (TS) table

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Detailed information is provided in the service information (SI) prime transport stream (TS) table

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
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
 

 

