---
UID: NF:mpeg2psiparser.IPAT.GetNextTable
title: IPAT::GetNextTable
author: windows-sdk-content
description: The GetNextTable method retrieves the next table that follows the current table.
old-location: mstv\ipat_getnexttable.htm
tech.root: mstv
ms.assetid: 24cc3c97-60f6-440d-80fd-da7516698a2e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNextTable, GetNextTable method [Microsoft TV Technologies], GetNextTable method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetNextTable method, IPAT.GetNextTable, IPAT::GetNextTable, IPATGetNextTable, mpeg2psiparser/IPAT::GetNextTable, mstv.ipat_getnexttable
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
 - IPAT.GetNextTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPAT::GetNextTable


## -description



The <b>GetNextTable</b> method retrieves the <i>next</i> table that follows the current table.




## -parameters




### -param ppPAT [out]

Address of a variable that receives an <b>IPAT</b> interface pointer. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

