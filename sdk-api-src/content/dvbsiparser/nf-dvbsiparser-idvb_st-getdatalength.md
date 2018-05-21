---
UID: NF:dvbsiparser.IDVB_ST.GetDataLength
title: IDVB_ST::GetDataLength
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_st_getdatalength.htm
old-project: mstv
ms.assetid: 6d42f147-b82d-4236-9e58-c42019d6b413
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetDataLength, GetDataLength method [Microsoft TV Technologies], GetDataLength method [Microsoft TV Technologies],IDVB_ST interface, IDVB_ST interface [Microsoft TV Technologies],GetDataLength method, IDVB_ST.GetDataLength, IDVB_ST::GetDataLength, IDVB_STGetDataLength, dvbsiparser/IDVB_ST::GetDataLength, mstv.idvb_st_getdatalength
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
-	IDVB_ST.GetDataLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_ST::GetDataLength


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetDataLength</b> method returns the length of the data in the ST.


## -parameters




### -param pwVal [out]

Pointer to a variable that receives the length, in bytes.


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




<a href="https://msdn.microsoft.com/56d77564-4de3-4252-9218-a1188f363437">IDVB_ST Interface</a>
 

 

