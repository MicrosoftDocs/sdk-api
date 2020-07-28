---
UID: NF:mpeg2psiparser.ICAT.GetTableDescriptorByTag
title: ICAT::GetTableDescriptorByTag (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTableDescriptorByTag","GetTableDescriptorByTag method [Microsoft TV Technologies]","GetTableDescriptorByTag method [Microsoft TV Technologies]","ICAT interface","ICAT interface [Microsoft TV Technologies]","GetTableDescriptorByTag method","ICAT.GetTableDescriptorByTag","ICAT::GetTableDescriptorByTag","ICATGetTableDescriptorByTag","mpeg2psiparser/ICAT::GetTableDescriptorByTag","mstv.icat_gettabledescriptorbytag"]
old-location: mstv\icat_gettabledescriptorbytag.htm
tech.root: mstv
ms.assetid: f28fb2c1-d9bb-4786-b3cc-db9583752e1b
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByTag, GetTableDescriptorByTag method [Microsoft TV Technologies], GetTableDescriptorByTag method [Microsoft TV Technologies],ICAT interface, ICAT interface [Microsoft TV Technologies],GetTableDescriptorByTag method, ICAT.GetTableDescriptorByTag, ICAT::GetTableDescriptorByTag, ICATGetTableDescriptorByTag, mpeg2psiparser/ICAT::GetTableDescriptorByTag, mstv.icat_gettabledescriptorbytag
f1_keywords:
- mpeg2psiparser/ICAT.GetTableDescriptorByTag
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mpeg2psiparser.h
api_name:
- ICAT.GetTableDescriptorByTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICAT::GetTableDescriptorByTag


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTableDescriptorByTag</b> method searches the CAT for a descriptor with the specified descriptor tag.


## -parameters




### -param bTag [in]

Specifies the descriptor tag for which to search.


### -param pdwCookie [in, out]

Pointer to a variable that specifies the start position in the descriptor list. This parameter is optional. If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the first descriptor in the list. Otherwise, the search starts from the position given in <i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i> parameter contains the position of the next matching descriptor, if any. You can use this parameter to iterate through the descriptor list, looking for every instance of a particular descriptor tag.


### -param ppDescriptor [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


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



If the value of <i>pdwCookie</i> is not <b>NULL</b>, the method returns either MPEG2_S_NO_MORE_DATA_AVAILABLE or MPEG2_S_MORE_DATA_AVAILABLE to indicate whether the MGT contains additional tags that match the search criteria.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-icat">ICAT Interface</a>
 

 

