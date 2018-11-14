---
UID: NF:dvbsiparser.IDVB_RST.GetCountOfRecords
title: IDVB_RST::GetCountOfRecords
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_rst_getcountofrecords.htm
tech.root: MSTV
ms.assetid: 98e71d2e-d84e-4be5-b779-0d7c10a823d5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDVB_RST interface, IDVB_RST interface [Microsoft TV Technologies],GetCountOfRecords method, IDVB_RST.GetCountOfRecords, IDVB_RST::GetCountOfRecords, IDVB_RSTGetCountOfRecords, dvbsiparser/IDVB_RST::GetCountOfRecords, mstv.idvb_rst_getcountofrecords
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDVB_RST.GetCountOfRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IDVB_RST.GetCountOfRecords
: 
---

# IDVB_RST::GetCountOfRecords


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfRecords</b> method returns the number of records in the RST.


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




<a href="https://msdn.microsoft.com/deee44cb-92b8-4d10-91d7-c99324ab5832">IDVB_RST Interface</a>
 

 

