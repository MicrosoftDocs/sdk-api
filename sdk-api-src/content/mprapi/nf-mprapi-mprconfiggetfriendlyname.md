---
UID: NF:mprapi.MprConfigGetFriendlyName
title: MprConfigGetFriendlyName function (mprapi.h)
author: windows-sdk-content
description: The MprConfigGetFriendlyName function returns the friendly name for an interface that corresponds to the specified GUID name.
old-location: rras\mprconfiggetfriendlyname.htm
tech.root: RRAS
ms.assetid: 16cd38f2-5029-4b95-871d-a8ba6c96b78c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprConfigGetFriendlyName, MprConfigGetFriendlyName function [RAS], _mpr_mprconfiggetfriendlyname, mprapi/MprConfigGetFriendlyName, rras.mprconfiggetfriendlyname
ms.topic: function
f1_keywords: 
 - "mprapi/MprConfigGetFriendlyName"
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
 - MprConfigGetFriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprConfigGetFriendlyName function


## -description


The 
<b>MprConfigGetFriendlyName</b> function returns the friendly name for an interface that corresponds to the specified GUID name.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.


### -param pszGuidName [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the GUID name for the interface.


### -param pszBuffer [out]

Pointer to a buffer that receives the friendly name for the interface.


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
One of the following parameters <i>hMprConfig</i>, <i>pszGuidName</i>, or <i>pszBuffer</i> is <b>NULL</b>.

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





## -remarks



For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecBP/avoiding-buffer-overruns">Avoiding Buffer Overruns</a>.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecBP/avoiding-buffer-overruns">Avoiding Buffer Overruns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprconfiggetguidname">MprConfigGetGuidName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
 

 

