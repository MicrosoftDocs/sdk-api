---
UID: NF:ras.RasClearLinkStatistics
title: RasClearLinkStatistics function
author: windows-sdk-content
description: The RasClearLinkStatistics functions clears any accumulated statistics for the specified link in a RAS multilink connection.
old-location: rras\rasclearlinkstatistics.htm
tech.root: rras
ms.assetid: cac356a9-092c-4db2-b0a4-aaacfc514e29
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RasClearLinkStatistics, RasClearLinkStatistics function [RAS], _ras_rasclearlinkstatistics, ras/RasClearLinkStatistics, rras.rasclearlinkstatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasClearLinkStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasClearLinkStatistics function


## -description


The 
<b>RasClearLinkStatistics</b> functions clears any accumulated statistics for the specified link in a RAS multilink connection.


## -parameters




### -param hRasConn [in]

Handle to the connection. Use 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> to obtain this handle.


### -param dwSubEntry [in]

Specifies the subentry that corresponds to the link for which to clear statistics.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hRasConn</i> parameter does not specify a valid connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSubEntry</i> parameter is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
RAS could not find a connected port that corresponds to the value in the <i>dwSubEntry</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate sufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b5c87ecd-4f21-46b5-91a3-41706907157a">RasClearConnectionStatistics</a>



<a href="https://msdn.microsoft.com/825a80c9-8023-4b7f-a303-f1eaa650e1d8">RasGetLinkStatistics</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

