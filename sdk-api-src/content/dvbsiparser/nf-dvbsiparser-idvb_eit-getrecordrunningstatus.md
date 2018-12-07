---
UID: NF:dvbsiparser.IDVB_EIT.GetRecordRunningStatus
title: IDVB_EIT::GetRecordRunningStatus
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_eit_getrecordrunningstatus.htm
tech.root: mstv
ms.assetid: fc5d4bc7-4d56-453f-90ed-6187f55ea464
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordRunningStatus, GetRecordRunningStatus method [Microsoft TV Technologies], GetRecordRunningStatus method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetRecordRunningStatus method, IDVB_EIT.GetRecordRunningStatus, IDVB_EIT::GetRecordRunningStatus, IDVB_EITGetRecordRunningStatus, dvbsiparser/IDVB_EIT::GetRecordRunningStatus, mstv.idvb_eit_getrecordrunningstatus
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
 - IDVB_EIT.GetRecordRunningStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_EIT::GetRecordRunningStatus


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRunningStatus</b> method returns the running status of a particular event in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number for the event, indexed from zero. Call <a href="https://msdn.microsoft.com/1ea8c91b-f1a2-4c04-933c-c8a2fbfda86f">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.


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




<a href="https://msdn.microsoft.com/86280e1e-09c3-45a4-bdfb-53eda8e5700e">IDVB_EIT Interface</a>
 

 

