---
UID: NF:dvbsiparser.IDVB_SIT.GetCountOfTableDescriptors
title: IDVB_SIT::GetCountOfTableDescriptors method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sit_getcountoftabledescriptors.htm
old-project: mstv
ms.assetid: 7fe03fe0-f12e-43cb-b340-26fffdf2d873
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies], IDVB_SIT interface, GetCountOfTableDescriptors,IDVB_SIT.GetCountOfTableDescriptors, IDVB_SIT, IDVB_SIT interface [Microsoft TV Technologies], GetCountOfTableDescriptors method, IDVB_SIT::GetCountOfTableDescriptors, IDVB_SITGetCountOfTableDescriptors, dvbsiparser/IDVB_SIT::GetCountOfTableDescriptors, mstv.idvb_sit_getcountoftabledescriptors
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
-	IDVB_SIT.GetCountOfTableDescriptors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SIT::GetCountOfTableDescriptors method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of table-wide descriptors in the SIT.


## -parameters




### -param pdwVal [out]

Pointer to a variable that receives the number of descriptors.


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




<a href="https://msdn.microsoft.com/f278d942-a450-4a01-998d-4dac1c8a1fcc">IDVB_SIT Interface</a>
 

 

