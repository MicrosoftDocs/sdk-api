---
UID: NF:mpeg2psiparser.ITSDT.RegisterForNextTable
title: ITSDT::RegisterForNextTable
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\itsdt_registerfornexttable.htm
tech.root: MSTV
ms.assetid: 36d597e2-0a65-48f3-8220-bb3481185af7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ITSDT interface [Microsoft TV Technologies],RegisterForNextTable method, ITSDT.RegisterForNextTable, ITSDT::RegisterForNextTable, ITSDTRegisterForNextTable, RegisterForNextTable, RegisterForNextTable method [Microsoft TV Technologies], RegisterForNextTable method [Microsoft TV Technologies],ITSDT interface, mpeg2psiparser/ITSDT::RegisterForNextTable, mstv.itsdt_registerfornexttable
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
 - ITSDT.RegisterForNextTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mpeg2psiparser.h
: 
- ITSDT.RegisterForNextTable
: 
---

# ITSDT::RegisterForNextTable


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>RegisterForNextTable</b> method registers the client to be notified when a <i>next</i> table arrives that will replace the current table.


## -parameters




### -param hNextTableAvailable [in]

Handle to an event created by the caller. The object signals the event when the <i>next</i> table arrives. When the event is signaled, call the <a href="https://msdn.microsoft.com/7b60647a-b668-4884-967d-044ff0d149c2">ITSDT::GetNextTable</a> method to retrieve the table.


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
This table is already a <i>next</i> table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>hNextTableAvailable</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The method has already been called.

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




<a href="https://msdn.microsoft.com/58ec73dc-79bd-415b-b9be-8e9246166391">ITSDT Interface</a>
 

 

