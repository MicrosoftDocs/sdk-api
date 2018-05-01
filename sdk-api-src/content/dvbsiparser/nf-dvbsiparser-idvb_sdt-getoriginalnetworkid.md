---
UID: NF:dvbsiparser.IDVB_SDT.GetOriginalNetworkId
title: IDVB_SDT::GetOriginalNetworkId method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sdt_getoriginalnetworkid.htm
old-project: mstv
ms.assetid: 4feebc95-cdcf-443c-bbc1-969575cb795f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetOriginalNetworkId method [Microsoft TV Technologies], GetOriginalNetworkId method [Microsoft TV Technologies], IDVB_SDT interface, GetOriginalNetworkId,IDVB_SDT.GetOriginalNetworkId, IDVB_SDT, IDVB_SDT interface [Microsoft TV Technologies], GetOriginalNetworkId method, IDVB_SDT::GetOriginalNetworkId, IDVB_SDTGetOriginalNetworkId, dvbsiparser/IDVB_SDT::GetOriginalNetworkId, mstv.idvb_sdt_getoriginalnetworkid
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
-	IDVB_SDT.GetOriginalNetworkId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SDT::GetOriginalNetworkId method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetOriginalNetworkId</b> method returns the original network identifier.


## -parameters




### -param pwVal [out]

Pointer to a variable that receives the original_network_id field. This value identifies the network_id of the originating delivery system.


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




<a href="https://msdn.microsoft.com/bb473a7e-8957-4e85-98d0-13c6992fbf37">IDVB_SDT Interface</a>
 

 

