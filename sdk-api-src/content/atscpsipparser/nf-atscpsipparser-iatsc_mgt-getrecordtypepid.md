---
UID: NF:atscpsipparser.IATSC_MGT.GetRecordTypePid
title: IATSC_MGT::GetRecordTypePid method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_mgt_getrecordtypepid.htm
old-project: mstv
ms.assetid: c8c4cfba-b03c-478e-a49e-c01d663535a0
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordTypePid method [Microsoft TV Technologies], GetRecordTypePid method [Microsoft TV Technologies], IATSC_MGT interface, GetRecordTypePid,IATSC_MGT.GetRecordTypePid, IATSC_MGT, IATSC_MGT interface [Microsoft TV Technologies], GetRecordTypePid method, IATSC_MGT::GetRecordTypePid, IATSC_MGTGetRecordTypePid, atscpsipparser/IATSC_MGT::GetRecordTypePid, mstv.iatsc_mgt_getrecordtypepid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_MGT.GetRecordTypePid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_MGT::GetRecordTypePid method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordTypePid</b> method returns the packet identifier (PID) for the table type described by a record in the MGT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/9f0c7f28-3280-4c2a-a030-68326eac23f0">IATSC_MGT::GetCountOfRecords</a> method to get the number of records in the MGT.


### -param ppidVal [out]

Receives the table_type_PID field.


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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

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




<a href="https://msdn.microsoft.com/2d6cc17f-7288-468c-a028-31e6e284d8ca">IATSC_MGT Interface</a>
 

 

