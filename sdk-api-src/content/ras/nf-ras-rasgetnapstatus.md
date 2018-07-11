---
UID: NF:ras.RasGetNapStatus
title: RasGetNapStatus function
author: windows-sdk-content
description: Retrieves the Network Access Protection (NAP) connection state variables for a given remote access connection.
old-location: rras\rasgetnapstatus.htm
old-project: rras
ms.assetid: 7f36f93f-7e07-4ad8-923f-59146bda4687
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: RasGetNapStatus, ras/rasgetnapstatus, rasgetnapstatus, rasgetnapstatus function [RAS], rras.rasgetnapstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - rasgetnapstatus
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasGetNapStatus function


## -description


The <b>RasGetNapStatus</b> function retrieves the <a href="https://msdn.microsoft.com/f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e">Network Access Protection</a> (NAP) connection state variables for a given remote access connection.


## -parameters




### -param hRasconn

TBD


### -param pRasNapState

TBD




#### - hRasConn [in]

A handle to the connection. Use <a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or <a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> to obtain this handle. 
					


#### - pNapState [in, out]

A pointer to a <a href="https://msdn.microsoft.com/1cba931c-041a-4ec6-8c30-db3a02b59ec3">RASNAPSTATE</a> structure. On input, the <b>dwSize</b> member of the structure must be set to <b>sizeof(RASNAPSTATE)</b>. On output, <i>pNapState</i> returns the NAP state of the RAS connection.
 


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_NAP_CAPABLE</b></dt>
</dl>
</td>
<td width="60%">
Connection corresponding to the <i>hRasConn</i> parameter is not configured for NAP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSize</i> parameter of the <a href="https://msdn.microsoft.com/1cba931c-041a-4ec6-8c30-db3a02b59ec3">RASNAPSTATE</a> structure has an invalid size value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Handle passed to the function is either <b>NULL</b> or invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
RASMAN could not find the handle in its list of handles.

</td>
</tr>
</table>
 



