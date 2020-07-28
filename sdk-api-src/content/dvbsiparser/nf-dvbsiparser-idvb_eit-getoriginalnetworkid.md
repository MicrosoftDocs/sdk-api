---
UID: NF:dvbsiparser.IDVB_EIT.GetOriginalNetworkId
title: IDVB_EIT::GetOriginalNetworkId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetOriginalNetworkId","GetOriginalNetworkId method [Microsoft TV Technologies]","GetOriginalNetworkId method [Microsoft TV Technologies]","IDVB_EIT interface","IDVB_EIT interface [Microsoft TV Technologies]","GetOriginalNetworkId method","IDVB_EIT.GetOriginalNetworkId","IDVB_EIT::GetOriginalNetworkId","IDVB_EITGetOriginalNetworkId","dvbsiparser/IDVB_EIT::GetOriginalNetworkId","mstv.idvb_eit_getoriginalnetworkid"]
old-location: mstv\idvb_eit_getoriginalnetworkid.htm
tech.root: mstv
ms.assetid: 8e477089-faef-4578-ac7f-fea7f1037dfc
ms.date: 12/05/2018
ms.keywords: GetOriginalNetworkId, GetOriginalNetworkId method [Microsoft TV Technologies], GetOriginalNetworkId method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetOriginalNetworkId method, IDVB_EIT.GetOriginalNetworkId, IDVB_EIT::GetOriginalNetworkId, IDVB_EITGetOriginalNetworkId, dvbsiparser/IDVB_EIT::GetOriginalNetworkId, mstv.idvb_eit_getoriginalnetworkid
f1_keywords:
- dvbsiparser/IDVB_EIT.GetOriginalNetworkId
dev_langs:
- c++
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
- IDVB_EIT.GetOriginalNetworkId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_EIT::GetOriginalNetworkId


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>
 

 

