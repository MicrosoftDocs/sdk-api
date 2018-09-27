---
UID: NF:icm.GetCMMInfo
title: GetCMMInfo function
author: windows-sdk-content
description: The GetCMMInfo function retrieves various information about the color management module (CMM) that created the specified color transform.
old-location: wcs\getcmminfo.htm
tech.root: WCS
ms.assetid: 60fe282c-ed52-45c8-ac64-03c2c684679c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CMM_DLL_VERSION, CMM_IDENT, CMM_WIN_VERSION, GetCMMInfo, GetCMMInfo function [Windows Color System], _color_GetCMMInfo, icm/GetCMMInfo, wcs.getcmminfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
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
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - GetCMMInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCMMInfo function


## -description


The <b>GetCMMInfo</b> function retrieves various information about the color management module (CMM) that created the specified color transform.


## -parameters




### -param hColorTransform

Identifies the transform for which to find CMM information.


### -param arg1

TBD




#### - dwInfo

Specifies the information to be retrieved. This parameter can take one of the following constant values.<div> </div>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMM_WIN_VERSION"></a><a id="cmm_win_version"></a><dl>
<dt><b>CMM_WIN_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the version of Windows targeted by the color management module (CMM).

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_DLL_VERSION"></a><a id="cmm_dll_version"></a><dl>
<dt><b>CMM_DLL_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the version number of the CMM.

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_IDENT"></a><a id="cmm_ident"></a><dl>
<dt><b>CMM_IDENT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the CMM signature registered with the International Color Consortium (ICC).

</td>
</tr>
</table>
 


## -returns



If this function succeeds, the return value is the information specified in <i>dwInfo.</i>

If this function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

