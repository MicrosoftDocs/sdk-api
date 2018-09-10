---
UID: NF:mpeg2psiparser.ITSDT.GetTableDescriptorByTag
title: ITSDT::GetTableDescriptorByTag
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\itsdt_gettabledescriptorbytag.htm
tech.root: mstv
ms.assetid: cb2f544b-02fd-4a48-838f-56815710a5bd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTableDescriptorByTag, GetTableDescriptorByTag method [Microsoft TV Technologies], GetTableDescriptorByTag method [Microsoft TV Technologies],ITSDT interface, ITSDT interface [Microsoft TV Technologies],GetTableDescriptorByTag method, ITSDT.GetTableDescriptorByTag, ITSDT::GetTableDescriptorByTag, ITSDTGetTableDescriptorByTag, mpeg2psiparser/ITSDT::GetTableDescriptorByTag, mstv.itsdt_gettabledescriptorbytag
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - ITSDT.GetTableDescriptorByTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSDT::GetTableDescriptorByTag


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetTableDescriptorByTag</b> method searches the TSDT for a descriptor with the specified descriptor tag.


## -parameters




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



If the value of <i>pdwCookie</i> is not <b>NULL</b>, the method returns either MPEG2_S_NO_MORE_DATA_AVAILABLE or MPEG2_S_MORE_DATA_AVAILABLE to indicate whether the MGT contains additional tags that match the search criteria.




## -see-also




<a href="https://msdn.microsoft.com/58ec73dc-79bd-415b-b9be-8e9246166391">ITSDT Interface</a>
 

 

