---
UID: NF:dvbsiparser.IDVB_BAT.ConvertNextToCurrent
title: IDVB_BAT::ConvertNextToCurrent
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_bat_convertnexttocurrent.htm
old-project: mstv
ms.assetid: befcd47c-e05e-4a75-a588-bebdb1cc3218
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ConvertNextToCurrent, ConvertNextToCurrent method [Microsoft TV Technologies], ConvertNextToCurrent method [Microsoft TV Technologies],IDVB_BAT interface, IDVB_BAT interface [Microsoft TV Technologies],ConvertNextToCurrent method, IDVB_BAT.ConvertNextToCurrent, IDVB_BAT::ConvertNextToCurrent, IDVB_BATConvertNextToCurrent, dvbsiparser/IDVB_BAT::ConvertNextToCurrent, mstv.idvb_bat_convertnexttocurrent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDVB_BAT.ConvertNextToCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_BAT::ConvertNextToCurrent


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>ConvertNextToCurrent</b> method converts a <i>next</i> table to a <i>current</i> table.


## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



This method applies only to <i>next</i> tables that have become current. Before calling this method, call <a href="https://msdn.microsoft.com/d68cd8f7-e152-4105-8bc3-e9dad68e4e68">IDVB_BAT::RegisterForWhenCurrent</a> and wait for the event to be signaled.




## -see-also




<a href="https://msdn.microsoft.com/c312a152-21ee-4708-90a8-ab9bde9a2011">IDVB_BAT Interface</a>
 

 

