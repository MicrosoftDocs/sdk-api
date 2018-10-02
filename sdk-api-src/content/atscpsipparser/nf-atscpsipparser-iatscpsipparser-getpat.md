---
UID: NF:atscpsipparser.IAtscPsipParser.GetPAT
title: IAtscPsipParser::GetPAT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatscpsipparser_getpat.htm
tech.root: MSTV
ms.assetid: 7cfa9ec0-a802-4dbe-9997-d0eaac2b71c9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPAT, GetPAT method [Microsoft TV Technologies], GetPAT method [Microsoft TV Technologies],IAtscPsipParser interface, IAtscPsipParser interface [Microsoft TV Technologies],GetPAT method, IAtscPsipParser.GetPAT, IAtscPsipParser::GetPAT, IAtscPsipParserGetPAT, atscpsipparser/IAtscPsipParser::GetPAT, mstv.iatscpsipparser_getpat
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
 - IAtscPsipParser.GetPAT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAtscPsipParser::GetPAT


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetPAT</b> method retrieves the program association table (PAT).


## -parameters




### -param ppPAT [out]

Receives an <a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT</a> interface pointer. The caller must release the interface.


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
NULL pointer argument.

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
 

 

