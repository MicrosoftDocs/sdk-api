---
UID: NF:mprapi.MprConfigGetGuidName
title: MprConfigGetGuidName function
author: windows-sdk-content
description: The MprConfigGetGuidName function returns the GUID name for an interface that corresponds to the specified friendly name.
old-location: rras\mprconfiggetguidname.htm
tech.root: rras
ms.assetid: 017662f7-7974-4598-a729-19181ccdfbe0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: MprConfigGetGuidName, MprConfigGetGuidName function [RAS], _mpr_mprconfiggetguidname, mprapi/MprConfigGetGuidName, rras.mprconfiggetguidname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - MprConfigGetGuidName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigGetGuidName function


## -description


The 
<b>MprConfigGetGuidName</b> function returns the GUID name for an interface that corresponds to the specified friendly name.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param pszFriendlyName [in]

Pointer to a Unicode string that specifies the friendly name for the interface.


### -param pszBuffer [out]

Pointer to a buffer that receives the GUID name for the interface.


### -param dwBufferSize [in]

Specifies the size, in bytes, of the buffer pointed to by <i>pszBuffer</i>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>pszBuffer</i> is not large enough to hold the returned GUID name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the parameters <i>hMprConfig</i>, <i>pszFriendlyName</i>, or <i>pszBuffer</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No GUID name was found that corresponds to the specified friendly name.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/16cd38f2-5029-4b95-871d-a8ba6c96b78c">MprConfigGetFriendlyName</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

