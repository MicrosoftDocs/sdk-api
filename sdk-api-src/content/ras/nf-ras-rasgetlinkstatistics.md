---
UID: NF:ras.RasGetLinkStatistics
title: RasGetLinkStatistics function
author: windows-sdk-content
description: The RasGetLinkStatistics function retrieves accumulated statistics for the specified link in a RAS multilink connection.
old-location: rras\rasgetlinkstatistics.htm
tech.root: rras
ms.assetid: 825a80c9-8023-4b7f-a303-f1eaa650e1d8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RasGetLinkStatistics, RasGetLinkStatistics function [RAS], _ras_rasgetlinkstatistics, ras/RasGetLinkStatistics, rras.rasgetlinkstatistics
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
 - RasGetLinkStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasGetLinkStatistics function


## -description


The 
<b>RasGetLinkStatistics</b> function retrieves accumulated statistics for the specified link in a RAS multilink connection.


## -parameters




### -param hRasConn [in]

Handle to the connection. Use 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> to obtain this handle.


### -param dwSubEntry [in]

Specifies the subentry that corresponds to the link for which to retrieve statistics.


### -param lpStatistics [in, out]

Pointer to the 
<a href="https://msdn.microsoft.com/f55852f9-fa6f-480c-9c65-d6631d5270a0">RAS_STATS</a> structure that, on output, receives the statistics. 




On input, the <b>dwSize</b> member of this structure specifies the size of 
<a href="https://msdn.microsoft.com/f55852f9-fa6f-480c-9c65-d6631d5270a0">RAS_STATS</a>. Use sizeof(<b>RAS_STATS</b>) to obtain this size.

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
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: the <i>hRasConn</i> parameter is zero, the <i>dwSubEntry</i> parameter is zero, the <i>lpStatistics</i> parameter is <b>NULL</b>, or the value specified by the <b>dwSize</b> member of the 
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
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cac356a9-092c-4db2-b0a4-aaacfc514e29">RasClearLinkStatistics</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/2db03535-c2bd-4e04-a86f-e68fe5c1f805">RasGetConnectionStatistics</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

