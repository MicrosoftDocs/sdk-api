---
UID: NF:mpeg2psiparser.ITSDT.ConvertNextToCurrent
title: ITSDT::ConvertNextToCurrent
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\itsdt_convertnexttocurrent.htm
old-project: mstv
ms.assetid: a8ce79ed-516a-44bf-b9c9-ff6d693cdd30
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],ITSDT interface, ITSDT interface [Microsoft TV Technologies],ConvertNextToCurrent method, ITSDT.ConvertNextToCurrent, ITSDT::ConvertNextToCurrent, ITSDTConvertNextToCurrent, mpeg2psiparser/ITSDT::ConvertNextToCurrent, mstv.itsdt_convertnexttocurrent
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2PsiParser.h
api_name:
-	ITSDT.ConvertNextToCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ITSDT::ConvertNextToCurrent


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>ConvertNextToCurrent</b> method converts a <i>next</i> table to a <i>current</i> table.


## -parameters






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
This table is already current.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <b>RegisterForWhenCurrent</b> method was not called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The new <i>current</i> table is malformed.

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



This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="https://msdn.microsoft.com/f2ce7908-3650-4ecf-8014-6bae377dcb5c">ITSDT::RegisterForWhenCurrent</a> and wait for the event to be signaled.




## -see-also




<a href="https://msdn.microsoft.com/58ec73dc-79bd-415b-b9be-8e9246166391">ITSDT Interface</a>
 

 

