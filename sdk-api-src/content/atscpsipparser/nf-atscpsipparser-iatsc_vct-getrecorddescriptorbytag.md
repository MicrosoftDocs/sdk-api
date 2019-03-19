---
UID: NF:atscpsipparser.IATSC_VCT.GetRecordDescriptorByTag
title: IATSC_VCT::GetRecordDescriptorByTag (atscpsipparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_getrecorddescriptorbytag.htm
tech.root: mstv
ms.assetid: b8c975fe-6bf9-443d-b069-cb8e5e01affc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IATSC_VCT.GetRecordDescriptorByTag, IATSC_VCT::GetRecordDescriptorByTag, IATSC_VCTGetRecordDescriptorByTag, atscpsipparser/IATSC_VCT::GetRecordDescriptorByTag, mstv.iatsc_vct_getrecorddescriptorbytag
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
 - IATSC_VCT.GetRecordDescriptorByTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSC_VCT::GetRecordDescriptorByTag


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByTag</b> method searches a record in the VCT for a descriptor with a specified descriptor tag.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/a6a9f998-f8a8-4459-91f8-aa4a5206d190">IATSC_VCT::GetCountOfRecords</a> method to get the number of records in the VCT.


### -param bTag [in]

Specifies the descriptor tag for which to search.


### -param pdwCookie [in, out]

Pointer to a variable that specifies the start position in the descriptor list. This parameter is optional. If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the first descriptor in the list. Otherwise, the search starts from the position given in *<i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i> parameter contains the position of the next matching descriptor, if any. You can use this parameter to iterate through the descriptor list, looking for every instance of a particular descriptor tag.


### -param ppDescriptor [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd694093(v=VS.85).aspx">IGenericDescriptor</a> interface. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


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
<dt><b>MPEG2_E_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified tag was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MORE_DATA_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The record contains at least one more descriptor with this tag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_NO_MORE_DATA_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The record does not contain any more descriptors with this tag.

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



If the value of <i>pdwCookie</i> is not <b>NULL</b>, the method returns either MPEG2_S_NO_MORE_DATA_AVAILABLE or MPEG2_S_MORE_DATA_AVAILABLE to indicate whether the record contains additional tags that match the search criteria.




## -see-also




<a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT Interface</a>
 

 

