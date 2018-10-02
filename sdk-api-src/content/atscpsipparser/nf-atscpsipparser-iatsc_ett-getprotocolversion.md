---
UID: NF:atscpsipparser.IATSC_ETT.GetProtocolVersion
title: IATSC_ETT::GetProtocolVersion
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_ett_getprotocolversion.htm
tech.root: MSTV
ms.assetid: 2fc7673c-486a-48dc-a283-55fbef42a2b0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProtocolVersion, GetProtocolVersion method [Microsoft TV Technologies], GetProtocolVersion method [Microsoft TV Technologies],IATSC_ETT interface, IATSC_ETT interface [Microsoft TV Technologies],GetProtocolVersion method, IATSC_ETT.GetProtocolVersion, IATSC_ETT::GetProtocolVersion, IATSC_ETTGetProtocolVersion, atscpsipparser/IATSC_ETT::GetProtocolVersion, mstv.iatsc_ett_getprotocolversion
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_ETT.GetProtocolVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSC_ETT::GetProtocolVersion


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetProtocolVersion</b> method returns the protocol version of the table.


## -parameters




### -param pbVal [out]

Receives the protocol_version field.


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
 

 

