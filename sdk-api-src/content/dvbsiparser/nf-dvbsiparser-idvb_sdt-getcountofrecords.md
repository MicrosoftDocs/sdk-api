---
UID: NF:dvbsiparser.IDVB_SDT.GetCountOfRecords
title: IDVB_SDT::GetCountOfRecords
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sdt_getcountofrecords.htm
old-project: mstv
ms.assetid: 9815ba89-d5c2-4d13-8ed1-478953836bc7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetCountOfRecords method, IDVB_SDT.GetCountOfRecords, IDVB_SDT::GetCountOfRecords, IDVB_SDTGetCountOfRecords, dvbsiparser/IDVB_SDT::GetCountOfRecords, mstv.idvb_sdt_getcountofrecords
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
-	IDVB_SDT.GetCountOfRecords
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SDT::GetCountOfRecords


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfRecords</b> method returns the number of records in the SDT.


## -parameters




### -param pdwVal [out]

Pointer to a variable that receives the number of records.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bb473a7e-8957-4e85-98d0-13c6992fbf37">IDVB_SDT Interface</a>
 

 

