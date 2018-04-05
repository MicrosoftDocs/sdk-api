---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordIsHiddenBitSet
title: IATSC_VCT::GetRecordIsHiddenBitSet method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_getrecordishiddenbitset.htm
old-project: mstv
ms.assetid: ef02da20-7c81-4c0b-83fd-7e4c0a36ea1a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetRecordIsHiddenBitSet method [Microsoft TV Technologies], GetRecordIsHiddenBitSet method [Microsoft TV Technologies], IATSC_VCT interface, GetRecordIsHiddenBitSet,IATSC_VCT.GetRecordIsHiddenBitSet, IATSC_VCT, IATSC_VCT interface [Microsoft TV Technologies], GetRecordIsHiddenBitSet method, IATSC_VCT::GetRecordIsHiddenBitSet, IATSC_VCTGetRecordIsHiddenBitSet, atscpsipparser/IATSC_VCT::GetRecordIsHiddenBitSet, mstv.iatsc_vct_getrecordishiddenbitset
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
req.typenames: APPX_PACKAGE_WRITER_PAYLOAD_STREAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_VCT.GetRecordIsHiddenBitSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_VCT::GetRecordIsHiddenBitSet method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordIsHiddenBitSet</b> method queries whether the hidden bit is set for a particular record in the VCT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/a6a9f998-f8a8-4459-91f8-aa4a5206d190">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.


### -param pfVal [out]

Receives a Boolean value. The value is <b>TRUE</b> if the hidden bit is set. Otherwise, the value is <b>FALSE</b>. Hidden channels are not accessed by the user; for example, they might be used for test signals.


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




<a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT Interface</a>
 

 

