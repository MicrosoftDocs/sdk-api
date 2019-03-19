---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordCountOfDescriptors
title: IATSC_VCT::GetRecordCountOfDescriptors (atscpsipparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_getrecordcountofdescriptors.htm
tech.root: mstv
ms.assetid: 8d85f653-181f-467f-b278-8bc721f8ff22
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordCountOfDescriptors, GetRecordCountOfDescriptors method [Microsoft TV Technologies], GetRecordCountOfDescriptors method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordCountOfDescriptors method, IATSC_VCT.GetRecordCountOfDescriptors, IATSC_VCT::GetRecordCountOfDescriptors, IATSC_VCTGetRecordCountOfDescriptors, atscpsipparser/IATSC_VCT::GetRecordCountOfDescriptors, mstv.iatsc_vct_getrecordcountofdescriptors
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_VCT.GetRecordCountOfDescriptors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSC_VCT::GetRecordCountOfDescriptors


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCountOfDescriptors</b> method returns the number of descriptors for a record in the VCT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/a6a9f998-f8a8-4459-91f8-aa4a5206d190">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.


### -param pdwVal [out]

Receives the number of descriptors.


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
 

 

