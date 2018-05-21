---
UID: NF:dvbsiparser.IDVB_SDT.GetRecordRunningStatus
title: IDVB_SDT::GetRecordRunningStatus
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sdt_getrecordrunningstatus.htm
old-project: mstv
ms.assetid: a6e799b3-f90e-415f-a380-e90d69184fe2
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetRecordRunningStatus, GetRecordRunningStatus method [Microsoft TV Technologies], GetRecordRunningStatus method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetRecordRunningStatus method, IDVB_SDT.GetRecordRunningStatus, IDVB_SDT::GetRecordRunningStatus, IDVB_SDTGetRecordRunningStatus, dvbsiparser/IDVB_SDT::GetRecordRunningStatus, mstv.idvb_sdt_getrecordrunningstatus
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
-	IDVB_SDT.GetRecordRunningStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SDT::GetRecordRunningStatus


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRunningStatus</b> method returns the running status of a particular service in the SDT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number for the service, indexed from zero. Call <a href="https://msdn.microsoft.com/9815ba89-d5c2-4d13-8ed1-478953836bc7">IDVB_SDT::GetCountOfRecords</a> to get the number of records in the SDT.


### -param pbVal [out]

Pointer to a variable that receives the running_status field. See the Remarks section in the <a href="https://msdn.microsoft.com/ca0a0b3b-14a8-4456-85a0-51df559d04b8">IDVB_RST::GetRecordRunningStatus</a> method for more information.


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




<a href="https://msdn.microsoft.com/bb473a7e-8957-4e85-98d0-13c6992fbf37">IDVB_SDT Interface</a>
 

 

