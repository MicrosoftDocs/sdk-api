---
UID: NF:dvbsiparser.IDVB_SIT.RegisterForNextTable
title: IDVB_SIT::RegisterForNextTable
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sit_registerfornexttable.htm
old-project: mstv
ms.assetid: 794c2fb0-ff8d-47b0-9a74-ccdb257a12c7
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IDVB_SIT interface [Microsoft TV Technologies],RegisterForNextTable method, IDVB_SIT.RegisterForNextTable, IDVB_SIT::RegisterForNextTable, IDVB_SITRegisterForNextTable, RegisterForNextTable, RegisterForNextTable method [Microsoft TV Technologies], RegisterForNextTable method [Microsoft TV Technologies],IDVB_SIT interface, dvbsiparser/IDVB_SIT::RegisterForNextTable, mstv.idvb_sit_registerfornexttable
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDVB_SIT.RegisterForNextTable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SIT::RegisterForNextTable


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>RegisterForNextTable</b> method registers the client to be notified when a <i>next</i> table arrives that will replace the current table.


## -parameters




### -param hNextTableAvailable [in]

Handle to an event created by the caller. The object signals the event when the <i>next</i> table arrives. When the event is signaled, call the <a href="https://msdn.microsoft.com/e5a23ec2-8eff-42cb-abe2-bf4447406e8c">IDVB_SIT::GetNextTable</a> method to retrieve the table.


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




<a href="https://msdn.microsoft.com/f278d942-a450-4a01-998d-4dac1c8a1fcc">IDVB_SIT Interface</a>
 

 

