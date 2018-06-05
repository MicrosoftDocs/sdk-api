---
UID: NF:mpeg2psiparser.IPAT.ConvertNextToCurrent
title: IPAT::ConvertNextToCurrent
author: windows-sdk-content
description: The ConvertNextToCurrent method converts a next table to a current table.
old-location: mstv\ipat_convertnexttocurrent.htm
old-project: mstv
ms.assetid: 89a493b9-93d3-435f-a4dc-24f8f8e2d1bf
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],ConvertNextToCurrent method, IPAT.ConvertNextToCurrent, IPAT::ConvertNextToCurrent, IPATConvertNextToCurrent, mpeg2psiparser/IPAT::ConvertNextToCurrent, mstv.ipat_convertnexttocurrent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2PsiParser.h
api_name:
-	IPAT.ConvertNextToCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::ConvertNextToCurrent


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



This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="https://msdn.microsoft.com/2a7808b6-2e31-4cd9-a4cc-7a6a7cf46cd4">IPAT::RegisterForWhenCurrent</a> and wait for the event to be signaled.




## -see-also




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

