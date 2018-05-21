---
UID: NF:dvbsiparser.IDVB_DIT.GetTransitionFlag
title: IDVB_DIT::GetTransitionFlag
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_dit_gettransitionflag.htm
old-project: mstv
ms.assetid: 3db3ee1e-7fff-442d-9e78-7862b19c339a
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetTransitionFlag, GetTransitionFlag method [Microsoft TV Technologies], GetTransitionFlag method [Microsoft TV Technologies],IDVB_DIT interface, IDVB_DIT interface [Microsoft TV Technologies],GetTransitionFlag method, IDVB_DIT.GetTransitionFlag, IDVB_DIT::GetTransitionFlag, IDVB_DITGetTransitionFlag, dvbsiparser/IDVB_DIT::GetTransitionFlag, mstv.idvb_dit_gettransitionflag
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
-	IDVB_DIT.GetTransitionFlag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_DIT::GetTransitionFlag


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTransitionFlag</b> method queries whether the transition_flag bit is set.


## -parameters




### -param pfVal [out]

Pointer to a variable that receives a Boolean value. The value is <b>TRUE</b> if the transition_flag bit is set, or <b>FALSE</b> otherwise.


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
<b>NULL</b> pointer argument.

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




<a href="https://msdn.microsoft.com/8acbb1ac-100f-47b9-b8db-580d1a845946">IDVB_DIT Interface</a>
 

 

