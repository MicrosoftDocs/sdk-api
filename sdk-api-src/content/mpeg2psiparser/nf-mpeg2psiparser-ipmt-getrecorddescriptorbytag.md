---
UID: NF:mpeg2psiparser.IPMT.GetRecordDescriptorByTag
title: IPMT::GetRecordDescriptorByTag
author: windows-sdk-content
description: The GetRecordDescriptorByTag method searches a record in the PMT for a descriptor with a specified descriptor tag.
old-location: mstv\ipmt_getrecorddescriptorbytag.htm
old-project: mstv
ms.assetid: 7ed3dd22-331a-419a-ab30-5645e259e36a
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IPMT.GetRecordDescriptorByTag, IPMT::GetRecordDescriptorByTag, IPMTGetRecordDescriptorByTag, mpeg2psiparser/IPMT::GetRecordDescriptorByTag, mstv.ipmt_getrecorddescriptorbytag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2psiparser.h
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetRecordDescriptorByTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::GetRecordDescriptorByTag


## -description



The <b>GetRecordDescriptorByTag</b> method searches a record in the PMT for a descriptor with a specified descriptor tag.




## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/f4e5009b-4c0d-4d0c-b480-4030cedbdb97">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.


### -param bTag [in]

Specifies the descriptor tag for which to search.


### -param pdwCookie [in, out]

Pointer to a variable that specifies the start position in the descriptor list. This parameter is optional. If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the first descriptor in the list. Otherwise, the search starts from the position given in <i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i> parameter contains the position of the next matching descriptor, if any. You can use this parameter to iterate through the descriptor list, looking for every instance of a particular descriptor tag.


### -param ppDescriptor [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

