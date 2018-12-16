---
UID: NF:mprapi.MprConfigGetFriendlyName
title: MprConfigGetFriendlyName function
author: windows-sdk-content
description: The MprConfigGetFriendlyName function returns the friendly name for an interface that corresponds to the specified GUID name.
old-location: rras\mprconfiggetfriendlyname.htm
tech.root: rras
ms.assetid: 16cd38f2-5029-4b95-871d-a8ba6c96b78c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprConfigGetFriendlyName, MprConfigGetFriendlyName function [RAS], _mpr_mprconfiggetfriendlyname, mprapi/MprConfigGetFriendlyName, rras.mprconfiggetfriendlyname
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
 - MprConfigGetFriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigGetFriendlyName function


## -description


The 
<b>MprConfigGetFriendlyName</b> function returns the friendly name for an interface that corresponds to the specified GUID name.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


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
<a href="https://msdn.microsoft.com/713fd6de-16af-49d2-8940-763c4a6e414b">Avoiding Buffer Overruns</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/713fd6de-16af-49d2-8940-763c4a6e414b">Avoiding Buffer Overruns</a>



<a href="https://msdn.microsoft.com/017662f7-7974-4598-a729-19181ccdfbe0">MprConfigGetGuidName</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

