---
UID: NF:atscpsipparser.IAtscPsipParser.GetETT
title: IAtscPsipParser::GetETT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatscpsipparser_getett.htm
tech.root: MSTV
ms.assetid: 6838620a-3dee-468e-bfc8-00757c06263e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetETT, GetETT method [Microsoft TV Technologies], GetETT method [Microsoft TV Technologies],IAtscPsipParser interface, IAtscPsipParser interface [Microsoft TV Technologies],GetETT method, IAtscPsipParser.GetETT, IAtscPsipParser::GetETT, IAtscPsipParserGetETT, atscpsipparser/IAtscPsipParser::GetETT, mstv.iatscpsipparser_getett
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
 - IAtscPsipParser.GetETT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- atscpsipparser.h
: 
- IAtscPsipParser.GetETT
: 
---

# IAtscPsipParser::GetETT


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetETT</b> method retrieves the extended text table (ETT).


## -parameters




### -param pid [in]

Specifies the packet identifier (PID) for the requested ETT.


### -param wSourceId [in]

Optional pointer to a variable that contains a table source identifier. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.


### -param pwEventId [in]

Optional pointer to a variable that contains a table event identifier. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.


### -param ppETT [out]

Receives an <a href="https://msdn.microsoft.com/ae52e81e-4de1-480c-82bf-c9629064970c">IATSC_ETT</a> interface pointer. The caller must release the interface.


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
 

 

