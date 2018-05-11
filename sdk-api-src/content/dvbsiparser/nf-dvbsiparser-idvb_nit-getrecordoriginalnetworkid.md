---
UID: NF:dvbsiparser.IDVB_NIT.GetRecordOriginalNetworkId
title: IDVB_NIT::GetRecordOriginalNetworkId
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_nit_getrecordoriginalnetworkid.htm
old-project: mstv
ms.assetid: 3179be9a-de2d-4cb3-ace2-ad5af66d35c8
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetRecordOriginalNetworkId, GetRecordOriginalNetworkId method [Microsoft TV Technologies], GetRecordOriginalNetworkId method [Microsoft TV Technologies],IDVB_NIT interface, IDVB_NIT interface [Microsoft TV Technologies],GetRecordOriginalNetworkId method, IDVB_NIT.GetRecordOriginalNetworkId, IDVB_NIT::GetRecordOriginalNetworkId, IDVB_NITGetRecordOriginalNetworkId, dvbsiparser/IDVB_NIT::GetRecordOriginalNetworkId, mstv.idvb_nit_getrecordoriginalnetworkid
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
-	IDVB_NIT.GetRecordOriginalNetworkId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_NIT::GetRecordOriginalNetworkId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordOriginalNetworkId</b> method returns the original network identifier for a record in the NIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/fb0f8071-575a-4bbd-b34b-b8d92c17c476">IDVB_NIT::GetCountOfRecords</a> method to get the number of records in the NIT.


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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

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
 

 

