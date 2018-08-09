---
UID: NF:dvbsiparser.IDVB_BAT.GetCountOfTableDescriptors
title: IDVB_BAT::GetCountOfTableDescriptors
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_bat_getcountoftabledescriptors.htm
old-project: mstv
ms.assetid: 8f373cbe-9d07-41c2-83a5-c25bc66f6263
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IDVB_BAT interface, IDVB_BAT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IDVB_BAT.GetCountOfTableDescriptors, IDVB_BAT::GetCountOfTableDescriptors, IDVB_BATGetCountOfTableDescriptors, dvbsiparser/IDVB_BAT::GetCountOfTableDescriptors, mstv.idvb_bat_getcountoftabledescriptors
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
 - IDVB_BAT.GetCountOfTableDescriptors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_BAT::GetCountOfTableDescriptors


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of table-wide descriptors in the BAT.


## -parameters




### -param pdwVal [out]

Pointer to a variable that receives the number of descriptors.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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




<a href="https://msdn.microsoft.com/c312a152-21ee-4708-90a8-ab9bde9a2011">IDVB_BAT Interface</a>
 

 

