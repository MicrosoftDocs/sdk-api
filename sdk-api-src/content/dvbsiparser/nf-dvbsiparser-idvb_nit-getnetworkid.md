---
UID: NF:dvbsiparser.IDVB_NIT.GetNetworkId
title: IDVB_NIT::GetNetworkId method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_nit_getnetworkid.htm
old-project: mstv
ms.assetid: 86841b62-d6c0-4911-baf7-dd6d1a08a770
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetNetworkId method [Microsoft TV Technologies], GetNetworkId method [Microsoft TV Technologies], IDVB_NIT interface, GetNetworkId,IDVB_NIT.GetNetworkId, IDVB_NIT, IDVB_NIT interface [Microsoft TV Technologies], GetNetworkId method, IDVB_NIT::GetNetworkId, IDVB_NITGetNetworkId, dvbsiparser/IDVB_NIT::GetNetworkId, mstv.idvb_nit_getnetworkid
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
-	IDVB_NIT.GetNetworkId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_NIT::GetNetworkId method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetNetworkId</b> method returns the network identifier for the NIT.


## -parameters




### -param pwVal [out]

Pointer to a variable that receives the network_id field.


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




<a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT Interface</a>
 

 

