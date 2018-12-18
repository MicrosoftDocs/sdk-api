---
UID: NF:ras.RasGetConnectionStatistics
title: RasGetConnectionStatistics function
author: windows-sdk-content
description: The RasGetConnectionStatistics function retrieves accumulated connection statistics for the specified connection.
old-location: rras\rasgetconnectionstatistics.htm
tech.root: rras
ms.assetid: 2db03535-c2bd-4e04-a86f-e68fe5c1f805
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RasGetConnectionStatistics, RasGetConnectionStatistics function [RAS], _ras_rasgetconnectionstatistics, ras/RasGetConnectionStatistics, rras.rasgetconnectionstatistics
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
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasGetConnectionStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasGetConnectionStatistics function


## -description


The 
<b>RasGetConnectionStatistics</b> function retrieves accumulated connection statistics for the specified connection.


## -parameters




### -param hRasConn [in]

Handle to the connection. Use <a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or <a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> to obtain this handle. 
					


### -param lpStatistics [in, out]

Pointer to the 
<a href="https://msdn.microsoft.com/f55852f9-fa6f-480c-9c65-d6631d5270a0">RAS_STATS</a> structure that, on output, receives the statistics. 




On input, set the <b>dwSize</b> member of this structure to sizeof(<a href="https://msdn.microsoft.com/f55852f9-fa6f-480c-9c65-d6631d5270a0">RAS_STATS</a>).

This parameter cannot be <b>NULL</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: the <i>hRasConn</i> parameter is zero, the <i>lpStatistics</i> parameter is <b>NULL</b>, or the value specified by the <b>dwSize</b> member of the 
<a href="https://msdn.microsoft.com/f55852f9-fa6f-480c-9c65-d6631d5270a0">RAS_STATS</a> structure specifies a version of the structure that is not supported by the operating system in use.

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



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/825a80c9-8023-4b7f-a303-f1eaa650e1d8">RasGetLinkStatistics</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

