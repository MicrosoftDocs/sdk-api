---
UID: NF:mpeg2psiparser.ICAT.ConvertNextToCurrent
title: ICAT::ConvertNextToCurrent
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icat_convertnexttocurrent.htm
tech.root: mstv
ms.assetid: bdd8f7a6-0c77-4058-bcca-9d712da781e0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],ICAT interface, ICAT interface [Microsoft TV Technologies],ConvertNextToCurrent method, ICAT.ConvertNextToCurrent, ICAT::ConvertNextToCurrent, ICATConvertNextToCurrent, mpeg2psiparser/ICAT::ConvertNextToCurrent, mstv.icat_convertnexttocurrent
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
 - mpeg2psiparser.h
api_name:
 - ICAT.ConvertNextToCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICAT::ConvertNextToCurrent


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



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



This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="https://msdn.microsoft.com/74a5c410-314e-4f49-b294-a4788e85cbef">ICAT::RegisterForWhenCurrent</a> and wait for the event to be signaled.




## -see-also




<a href="https://msdn.microsoft.com/00da2af8-0f1a-467a-b310-8b8c7e564013">ICAT Interface</a>
 

 

