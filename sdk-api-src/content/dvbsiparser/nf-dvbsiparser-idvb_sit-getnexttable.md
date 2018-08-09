---
UID: NF:dvbsiparser.IDVB_SIT.GetNextTable
title: IDVB_SIT::GetNextTable
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sit_getnexttable.htm
old-project: mstv
ms.assetid: e5a23ec2-8eff-42cb-abe2-bf4447406e8c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetNextTable, GetNextTable method [Microsoft TV Technologies], GetNextTable method [Microsoft TV Technologies],IDVB_SIT interface, IDVB_SIT interface [Microsoft TV Technologies],GetNextTable method, IDVB_SIT.GetNextTable, IDVB_SIT::GetNextTable, IDVB_SITGetNextTable, dvbsiparser/IDVB_SIT::GetNextTable, mstv.idvb_sit_getnexttable
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_SIT.GetNextTable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SIT::GetNextTable


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetNextTable</b> method retrieves the <i>next</i> table that follows the current table.


## -parameters




### -param dwTimeout [in]

Specifies a time-out value, in milliseconds. If the filter does not receive the data within the time-out period, the method fails.


### -param ppSIT [out]

Address of a variable that receives an <b>IDVB_SIT</b> interface pointer. The caller must release the interface.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This table is not current.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
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
 




## -remarks



This method applies only to <i>current</i> tables. Otherwise, the method returns E_ACCESSDENIED.




## -see-also




<a href="https://msdn.microsoft.com/f278d942-a450-4a01-998d-4dac1c8a1fcc">IDVB_SIT Interface</a>
 

 

