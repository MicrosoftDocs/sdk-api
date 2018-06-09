---
UID: NF:dvbsiparser.IDVB_NIT.GetVersionNumber
title: IDVB_NIT::GetVersionNumber
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_nit_getversionnumber.htm
old-project: mstv
ms.assetid: 75f7dc3b-8631-4a33-90f2-ace95e4112a7
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IDVB_NIT interface, IDVB_NIT interface [Microsoft TV Technologies],GetVersionNumber method, IDVB_NIT.GetVersionNumber, IDVB_NIT::GetVersionNumber, IDVB_NITGetVersionNumber, dvbsiparser/IDVB_NIT::GetVersionNumber, mstv.idvb_nit_getversionnumber
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
 - IDVB_NIT.GetVersionNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_NIT::GetVersionNumber


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetVersionNumber</b> method returns the version number for the NIT.


## -parameters




### -param pbVal [out]

Pointer to a variable that receives the version_number field.


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




<a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT Interface</a>
 

 

