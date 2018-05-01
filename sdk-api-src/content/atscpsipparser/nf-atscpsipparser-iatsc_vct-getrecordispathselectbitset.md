---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordIsPathSelectBitSet
title: IATSC_VCT::GetRecordIsPathSelectBitSet method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_getrecordispathselectbitset.htm
old-project: mstv
ms.assetid: 6f3e1e5c-0506-420d-981b-d30d77604e97
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordIsPathSelectBitSet method [Microsoft TV Technologies], GetRecordIsPathSelectBitSet method [Microsoft TV Technologies], IATSC_VCT interface, GetRecordIsPathSelectBitSet,IATSC_VCT.GetRecordIsPathSelectBitSet, IATSC_VCT, IATSC_VCT interface [Microsoft TV Technologies], GetRecordIsPathSelectBitSet method, IATSC_VCT::GetRecordIsPathSelectBitSet, IATSC_VCTGetRecordIsPathSelectBitSet, atscpsipparser/IATSC_VCT::GetRecordIsPathSelectBitSet, mstv.iatsc_vct_getrecordispathselectbitset
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
-	IATSC_VCT.GetRecordIsPathSelectBitSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_VCT::GetRecordIsPathSelectBitSet method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordIsPathSelectBitSet</b> method queries whether the path_select bit is set for a particular record in the VCT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/a6a9f998-f8a8-4459-91f8-aa4a5206d190">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.


### -param pfVal [out]

Receives a Boolean value. The value is <b>TRUE</b> if the path_select bit is set, or <b>FALSE</b> otherwise. The path_select bit indicates which physical input cable carries the transport stream.


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
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The table does not contain an out_of_band bit.

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
 




## -remarks



This bit applies only to cable VCTs. If the VCT is a terrestrial VCT, the method returns MPEG2_E_NOT_PRESENT.




## -see-also




<a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT Interface</a>
 

 

