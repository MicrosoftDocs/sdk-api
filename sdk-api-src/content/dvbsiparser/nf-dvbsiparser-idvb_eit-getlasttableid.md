---
UID: NF:dvbsiparser.IDVB_EIT.GetLastTableId
title: IDVB_EIT::GetLastTableId
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_eit_getlasttableid.htm
tech.root: MSTV
ms.assetid: b99ab578-fec3-457c-8be2-f0cb65c5b7f7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetLastTableId, GetLastTableId method [Microsoft TV Technologies], GetLastTableId method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetLastTableId method, IDVB_EIT.GetLastTableId, IDVB_EIT::GetLastTableId, IDVB_EITGetLastTableId, dvbsiparser/IDVB_EIT::GetLastTableId, mstv.idvb_eit_getlasttableid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_EIT.GetLastTableId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_EIT::GetLastTableId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetLastTableId</b> method returns the last table identifier used. If there are multiple EITs, the event information is chronological across successive table identifiers.


## -parameters




### -param pbVal [out]

Pointer to a variable that receives the last_table_id field.


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
 




## -see-also




<a href="https://msdn.microsoft.com/86280e1e-09c3-45a4-bdfb-53eda8e5700e">IDVB_EIT Interface</a>
 

 

