---
UID: NF:dvbsiparser.IDVB_EIT.GetVersionHash
title: IDVB_EIT::GetVersionHash method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_eit_getversionhash.htm
old-project: mstv
ms.assetid: 38b36718-2ec0-4983-8af5-669b05079ff0
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetVersionHash method [Microsoft TV Technologies], GetVersionHash method [Microsoft TV Technologies], IDVB_EIT interface, GetVersionHash,IDVB_EIT.GetVersionHash, IDVB_EIT, IDVB_EIT interface [Microsoft TV Technologies], GetVersionHash method, IDVB_EIT::GetVersionHash, IDVB_EITGetVersionHash, dvbsiparser/IDVB_EIT::GetVersionHash, mstv.idvb_eit_getversionhash
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
-	IDVB_EIT.GetVersionHash
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_EIT::GetVersionHash method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetVersionHash</b> method returns a hash value for this table instance. The hash value has the property that tables referring to the same content, but with different version_number and table_id fields, will return the same hash value. You can use this hash value to identify when two tables carry the same information, even if the tables are carried on different transport streams.


## -parameters




### -param pdwVersionHash






#### - pbVal [out]

Receives the hash value.


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
 

 

