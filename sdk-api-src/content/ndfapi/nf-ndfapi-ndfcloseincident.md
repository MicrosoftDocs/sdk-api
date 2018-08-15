---
UID: NF:ndfapi.NdfCloseIncident
title: NdfCloseIncident function
author: windows-sdk-content
description: Used to close an Network Diagnostics Framework (NDF) incident following its resolution.
old-location: ndf\ndfcloseincident.htm
old-project: ndf
ms.assetid: 5e5caf41-ca24-42e0-ac22-3b569400c383
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NdfCloseIncident, NdfCloseIncident function [NDF], ndf.ndfcloseincident, ndfapi/NdfCloseIncident
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ndfapi.h
req.include-header: 
req.redist: 
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
req.typenames: UiInfo, *PUiInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfCloseIncident
product: Windows
targetos: Windows
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdfCloseIncident function


## -description


The <b>NdfCloseIncident</b> function is used to close an Network Diagnostics Framework (NDF) incident following its resolution.


## -parameters




### -param handle [in]

Type: <b>NDFHANDLE</b>

Handle to the NDF incident that is being closed.


## -returns



Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8570a0e2-f02f-4812-a5c8-13b6e5feee6f">NdfCreateIncident</a>



<a href="https://msdn.microsoft.com/c4cb2713-b656-47a8-9de7-9d33e864a811">NdfCreateWinSockIncident</a>



<a href="https://msdn.microsoft.com/b65f30c3-53d5-4282-8d38-5723772f15fc">NdfExecuteDiagnosis</a>
 

 

