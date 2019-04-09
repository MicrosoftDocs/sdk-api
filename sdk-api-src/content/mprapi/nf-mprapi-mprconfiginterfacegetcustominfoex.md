---
UID: NF:mprapi.MprConfigInterfaceGetCustomInfoEx
title: MprConfigInterfaceGetCustomInfoEx function (mprapi.h)
author: windows-sdk-content
description: Retrieves the custom IKEv2 policy configuration for the specified interface.
old-location: rras\mprconfiginterfacegetcustominfoex.htm
tech.root: RRAS
ms.assetid: 97fa62f4-5e1c-4634-a3c7-974425717080
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprConfigInterfaceGetCustomInfoEx, MprConfigInterfaceGetCustomInfoEx function [RAS], mprapi/MprConfigInterfaceGetCustomInfoEx, rras.mprconfiginterfacegetcustominfoex
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigInterfaceGetCustomInfoEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigInterfaceGetCustomInfoEx function


## -description


Retrieves the custom IKEv2 policy configuration for the specified interface.


## -parameters




### -param hMprConfig [in]

The handle to the router configuration. This handle is obtained by calling the <a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a> function.


### -param hRouterInterface [in]

The handle to the interface configuration being updated. Obtain this handle by calling the  <a href="https://msdn.microsoft.com/e368aa3c-bb80-49ed-a1da-39777dada960">MprConfigInterfaceCreate</a> function, the <a href="https://msdn.microsoft.com/1088e587-4446-4463-b411-a11e34adaf6a">MprConfigInterfaceGetHandle</a> function, or the <a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a> function.


### -param pCustomInfo [out]

A pointer to a <a href="https://msdn.microsoft.com/53c4b7ae-db73-4d97-a99f-a98354c48a92">MPR_IF_CUSTOMINFOEX</a>  structure. When you have finished using the structure, free the buffer by calling the <a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a> function.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>. If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true:

<ul>
<li>The <i>hMprConfig</i> parameter is <b>NULL</b>.</li>
<li>The <i>hRouterInterface</i> parameter is <b>NULL</b>.</li>
<li>The <i>pCustomInfo</i> parameter is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There were insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface that corresponds to <i>hRouterInterface</i> parameter is not present in the router configuration.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

