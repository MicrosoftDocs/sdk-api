---
UID: NF:atscpsipparser.IAtscPsipParser.GetVCT
title: IAtscPsipParser::GetVCT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatscpsipparser_getvct.htm
old-project: mstv
ms.assetid: d3df008e-020f-4ed3-9422-2d5f0f0b865f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetVCT, GetVCT method [Microsoft TV Technologies], GetVCT method [Microsoft TV Technologies],IAtscPsipParser interface, IAtscPsipParser interface [Microsoft TV Technologies],GetVCT method, IAtscPsipParser.GetVCT, IAtscPsipParser::GetVCT, IAtscPsipParserGetVCT, atscpsipparser/IAtscPsipParser::GetVCT, mstv.iatscpsipparser_getvct
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
 - IAtscPsipParser.GetVCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAtscPsipParser::GetVCT


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetVCT</b> method retrieves the virtual channel table (VCT).


## -parameters




### -param tableId [in]

Specifies the table identifier (TID) of the VCT. Use one of the following values, declared in mpeg2data.h.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ATSC_VCT_CABL_TID (0xC9)</td>
<td>Cable</td>
</tr>
<tr>
<td>ATSC_VCT_TERR_TID (0xC8)</td>
<td>Terrestrial</td>
</tr>
</table>
 


### -param fGetNextTable [in]

Boolean value that indicates whether to search for the current table or the next table. If the value is <b>TRUE</b>, the method searches for a table with the current_next_indicator flag set to 1. Otherwise, the method searches for a table with the current_next_indicator flag set to 0.


### -param ppVCT [out]

Receives an <a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT</a> interface pointer. The caller must release the interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
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
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive the table in the allotted time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <b>Initialize</b> method was not called.

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



The method fails if the filter does not receive a matching table within a predetermined length of time.




## -see-also




<a href="https://msdn.microsoft.com/dbe922b3-b843-4eaa-807d-5608cfbb9686">IAtscPsipParser Interface</a>
 

 

