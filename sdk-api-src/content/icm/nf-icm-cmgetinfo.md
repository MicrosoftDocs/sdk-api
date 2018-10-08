---
UID: NF:icm.CMGetInfo
title: CMGetInfo function
author: windows-sdk-content
description: The CMGetInfo function retrieves various information about the color management module (CMM).
old-location: wcs\cmgetinfo.htm
tech.root: WCS
ms.assetid: 7a858c73-799c-4388-a83e-55e57f48a860
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: CMGetInfo, CMGetInfo function [Windows Color System], CMM_DESCRIPTION, CMM_DLL_VERSION, CMM_DRIVER_LEVEL, CMM_IDENT, CMM_LOGOICON, CMM_VERSION, CMM_WIN_VERSION, _color_CMGetInfo, icm/CMGetInfo, wcs.cmgetinfo
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
req.lib: Gdi32.lib
req.dll: Icm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - icm32.dll
api_name:
 - CMGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMGetInfo function


## -description


The <b>CMGetInfo</b> function retrieves various information about the color management module (CMM).

Every CMM is required to export this function.


## -parameters




### -param dwInfo

Specifies what information should be retrieved. This parameter can take one of the following constant values.<div> </div>


<table>
<tr>
<th>Constant</th>
<th>Significance of the function's return value</th>
</tr>
<tr>
<td width="40%"><a id="CMM_DESCRIPTION"></a><a id="cmm_description"></a><dl>
<dt><b>CMM_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
A text string that describes the color management module.

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_DLL_VERSION"></a><a id="cmm_dll_version"></a><dl>
<dt><b>CMM_DLL_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Version number of the CMM DLL.

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_DRIVER_LEVEL"></a><a id="cmm_driver_level"></a><dl>
<dt><b>CMM_DRIVER_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
Driver compatibility information.

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_IDENT"></a><a id="cmm_ident"></a><dl>
<dt><b>CMM_IDENT</b></dt>
</dl>
</td>
<td width="60%">
The CMM identification signature registered with the International Color Consortium (ICC).

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_LOGOICON"></a><a id="cmm_logoicon"></a><dl>
<dt><b>CMM_LOGOICON</b></dt>
</dl>
</td>
<td width="60%">
The logo icon for this CMM.

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_VERSION"></a><a id="cmm_version"></a><dl>
<dt><b>CMM_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Version of Windows supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CMM_WIN_VERSION"></a><a id="cmm_win_version"></a><dl>
<dt><b>CMM_WIN_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Backward compatibility with Windows 95.

</td>
</tr>
</table>
 


## -returns



If this function succeeds, the return value is the same nonzero value that was passed in through the <i>dwInfo</i> parameter. If the function fails, the return value is zero.




## -remarks



The <b>CMGetInfo</b> function can be called by applications directly to obtain information about the CMM. Applications should not call other CMM functions directly. To obtain CMM information, get the path to the CMM from the registry. Invoke the Windows API function <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> and pass the file name of the CMM as the value of its parameter. Call the <b>CMGetInfo</b> function and pass it the constant CMM_DESCRIPTION as the value of its parameter. Call the <a href="_win32_loadstring">LoadString</a> function. Pass the module handle as the first parameter, and the return value of the <b>CMGetInfo</b> function as the value of the second parameter.

CMMs that do not run on Windows 95 should return 0x0050000 for CMM_WIN_VERSION.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

