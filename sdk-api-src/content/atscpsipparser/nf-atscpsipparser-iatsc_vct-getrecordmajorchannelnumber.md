---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordMajorChannelNumber
title: IATSC_VCT::GetRecordMajorChannelNumber
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_getrecordmajorchannelnumber.htm
old-project: mstv
ms.assetid: 103de5b5-e78c-49a2-81a7-e85eae2d79c1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordMajorChannelNumber, GetRecordMajorChannelNumber method [Microsoft TV Technologies], GetRecordMajorChannelNumber method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordMajorChannelNumber method, IATSC_VCT.GetRecordMajorChannelNumber, IATSC_VCT::GetRecordMajorChannelNumber, IATSC_VCTGetRecordMajorChannelNumber, atscpsipparser/IATSC_VCT::GetRecordMajorChannelNumber, mstv.iatsc_vct_getrecordmajorchannelnumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: atscpsipparser.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_VCT.GetRecordMajorChannelNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_VCT::GetRecordMajorChannelNumber


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordMajorChannelNumber</b> method returns the major channel number for a record in the VCT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/a6a9f998-f8a8-4459-91f8-aa4a5206d190">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.


### -param pwVal [out]

Receives the major channel number.


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




<a href="https://msdn.microsoft.com/e0c6eecb-7543-4476-882c-29b1ee103359">GetRecordMinorChannelNumber</a>



<a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT Interface</a>
 

 

