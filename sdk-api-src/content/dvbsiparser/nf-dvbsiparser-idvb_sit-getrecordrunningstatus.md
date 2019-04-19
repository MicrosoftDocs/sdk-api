---
UID: NF:dvbsiparser.IDVB_SIT.GetRecordRunningStatus
title: IDVB_SIT::GetRecordRunningStatus (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sit_getrecordrunningstatus.htm
tech.root: mstv
ms.assetid: 223b7f11-b2fa-4f63-9c9d-bee02e721670
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordRunningStatus, GetRecordRunningStatus method [Microsoft TV Technologies], GetRecordRunningStatus method [Microsoft TV Technologies],IDVB_SIT interface, IDVB_SIT interface [Microsoft TV Technologies],GetRecordRunningStatus method, IDVB_SIT.GetRecordRunningStatus, IDVB_SIT::GetRecordRunningStatus, IDVB_SITGetRecordRunningStatus, dvbsiparser/IDVB_SIT::GetRecordRunningStatus, mstv.idvb_sit_getrecordrunningstatus
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
 - IDVB_SIT.GetRecordRunningStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_SIT::GetRecordRunningStatus


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRunningStatus</b> method returns the running status of a particular event in the SIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number for the event, indexed from zero. Call <a href="https://msdn.microsoft.com/93d04770-9ec5-411c-8892-4b9a7944d681">IDVB_SIT::GetCountOfRecords</a> to get the number of records in the SIT.


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




<a href="https://msdn.microsoft.com/f278d942-a450-4a01-998d-4dac1c8a1fcc">IDVB_SIT Interface</a>
 

 

