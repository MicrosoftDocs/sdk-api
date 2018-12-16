---
UID: NF:mpeg2psiparser.IPMT.GetNextTable
title: IPMT::GetNextTable
author: windows-sdk-content
description: The GetNextTable method retrieves the next table that follows the current table.
old-location: mstv\ipmt_getnexttable.htm
tech.root: mstv
ms.assetid: a1e6f321-b24b-46dc-8da8-5a4bbda61918
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNextTable, GetNextTable method [Microsoft TV Technologies], GetNextTable method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetNextTable method, IPMT.GetNextTable, IPMT::GetNextTable, IPMTGetNextTable, mpeg2psiparser/IPMT::GetNextTable, mstv.ipmt_getnexttable
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
 - IPMT.GetNextTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPMT::GetNextTable


## -description



The <b>GetNextTable</b> method retrieves the <i>next</i> table that follows the current table.




## -parameters




### -param ppPMT [out]

Address of a variable that receives an <b>IPMT</b> interface pointer. The caller must release the interface.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This table is not current.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method applies only to <i>current</i> tables. Otherwise, the method returns E_ACCESSDENIED.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694820(v=VS.85).aspx">IPMT Interface</a>
 

 

