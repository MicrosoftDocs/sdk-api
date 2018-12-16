---
UID: NF:mpeg2psiparser.IPMT.ConvertNextToCurrent
title: IPMT::ConvertNextToCurrent
author: windows-sdk-content
description: The ConvertNextToCurrent method converts a next table to a current table.
old-location: mstv\ipmt_convertnexttocurrent.htm
tech.root: mstv
ms.assetid: cc3eb6f3-c539-42c4-847a-5d1e80c53255
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],ConvertNextToCurrent method, IPMT.ConvertNextToCurrent, IPMT::ConvertNextToCurrent, IPMTConvertNextToCurrent, mpeg2psiparser/IPMT::ConvertNextToCurrent, mstv.ipmt_convertnexttocurrent
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
 - IPMT.ConvertNextToCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPMT::ConvertNextToCurrent


## -description



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



This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="https://msdn.microsoft.com/en-us/library/Dd694839(v=VS.85).aspx">IPMT::RegisterForWhenCurrent</a> and wait for the event to be signaled.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694820(v=VS.85).aspx">IPMT Interface</a>
 

 

