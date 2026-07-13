---
UID: NF:icm.CMGetInfo
title: CMGetInfo
description: Retrieves various information about the color management module (CMM).
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - icm.h
api_name:
 - CMGetInfo
f1_keywords:
 - CMGetInfo
 - icm/CMGetInfo
dev_langs:
 - c++
---

## -description

Retrieves various information about the color management module (CMM).

Every CMM is required to export this function.

## -parameters

### -param dwInfo

Specifies what information should be retrieved. This parameter can take one of the following constant values.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Constant</th>
<th>Significance of the function's return value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="CMM_DESCRIPTION"></span><span id="cmm_description"></span>
<strong>CMM_DESCRIPTION</strong></td>
<td><p>A text string that describes the color management module.</p></td>
</tr>
<tr class="even">
<td><span id="CMM_DLL_VERSION"></span><span id="cmm_dll_version"></span>
<strong>CMM_DLL_VERSION</strong></td>
<td><p>Version number of the CMM DLL.</p></td>
</tr>
<tr class="odd">
<td><span id="CMM_DRIVER_LEVEL"></span><span id="cmm_driver_level"></span>
<strong>CMM_DRIVER_LEVEL</strong></td>
<td><p>Driver compatibility information.</p></td>
</tr>
<tr class="even">
<td><span id="CMM_IDENT"></span><span id="cmm_ident"></span>
<strong>CMM_IDENT</strong></td>
<td><p>The CMM identification signature registered with the International Color Consortium (ICC).</p></td>
</tr>
<tr class="odd">
<td><span id="CMM_LOGOICON"></span><span id="cmm_logoicon"></span>
<strong>CMM_LOGOICON</strong></td>
<td><p>The logo icon for this CMM.</p></td>
</tr>
<tr class="even">
<td><span id="CMM_VERSION"></span><span id="cmm_version"></span>
<strong>CMM_VERSION</strong></td>
<td><p>Version of Windows supported.</p></td>
</tr>
<tr class="odd">
<td><span id="CMM_WIN_VERSION"></span><span id="cmm_win_version"></span>
<strong>CMM_WIN_VERSION</strong></td>
<td><p>Backward compatibility with Windows 95.</p></td>
</tr>
</tbody>
</table>

## -returns

If this function succeeds, the return value is the same nonzero value that was passed in through the *dwInfo* parameter. If the function fails, the return value is zero.

## -remarks

The **CMGetInfo** function can be called by applications directly to obtain information about the CMM. Applications should not call other CMM functions directly. To obtain CMM information, get the path to the CMM from the registry. Invoke the Windows API function [GetModuleHandle](../libloaderapi/nf-libloaderapi-getmodulehandlea.md) and pass the file name of the CMM as the value of its parameter. Call the **CMGetInfo** function and pass it the constant CMM\_DESCRIPTION as the value of its parameter. Call the [LoadString](../winuser/nf-winuser-loadstringa.md) function. Pass the module handle as the first parameter, and the return value of the **CMGetInfo** function as the value of the second parameter.

CMMs that do not run on Windows 95 should return 0x0050000 for CMM\_WIN\_VERSION.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
