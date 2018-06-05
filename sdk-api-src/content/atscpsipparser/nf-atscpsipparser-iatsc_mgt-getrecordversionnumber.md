---
UID: NF:atscpsipparser.IATSC_MGT.GetRecordVersionNumber
title: IATSC_MGT::GetRecordVersionNumber
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_mgt_getrecordversionnumber.htm
old-project: mstv
ms.assetid: 1a5ec8e9-d1e6-4514-8d0d-7992be52ba8c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordVersionNumber, GetRecordVersionNumber method [Microsoft TV Technologies], GetRecordVersionNumber method [Microsoft TV Technologies],IATSC_MGT interface, IATSC_MGT interface [Microsoft TV Technologies],GetRecordVersionNumber method, IATSC_MGT.GetRecordVersionNumber, IATSC_MGT::GetRecordVersionNumber, IATSC_MGTGetRecordVersionNumber, atscpsipparser/IATSC_MGT::GetRecordVersionNumber, mstv.iatsc_mgt_getrecordversionnumber
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_MGT.GetRecordVersionNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_MGT::GetRecordVersionNumber


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordVersionNumber</b> method returns the version number for the table type described by a record in the MGT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/9f0c7f28-3280-4c2a-a030-68326eac23f0">IATSC_MGT::GetCountOfRecords</a> method to get the number of records in the MGT.


### -param pbVal [out]

Receives the table_type_version_number field. This value should match the version_number field in the corresponding table.


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
 

 

