---
UID: NF:atscpsipparser.IATSC_ETT.GetEtmId
title: IATSC_ETT::GetEtmId
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_ett_getetmid.htm
old-project: mstv
ms.assetid: e45e6709-bb16-4644-b2d1-2ffd6d85f224
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEtmId, GetEtmId method [Microsoft TV Technologies], GetEtmId method [Microsoft TV Technologies],IATSC_ETT interface, IATSC_ETT interface [Microsoft TV Technologies],GetEtmId method, IATSC_ETT.GetEtmId, IATSC_ETT::GetEtmId, IATSC_ETTGetEtmId, atscpsipparser/IATSC_ETT::GetEtmId, mstv.iatsc_ett_getetmid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: atscpsipparser.h
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
req.typenames: AsyncStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_ETT.GetEtmId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_ETT::GetEtmId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetEtmId</b> method returns the ETM identifier, which is a unique 32-bit identifier for the text message.


## -parameters




### -param pdwVal [out]

Receives the ETM_id field.


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




<a href="https://msdn.microsoft.com/ae52e81e-4de1-480c-82bf-c9629064970c">IATSC_ETT Interface</a>
 

 

