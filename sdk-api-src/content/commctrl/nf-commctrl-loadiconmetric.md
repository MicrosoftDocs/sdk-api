---
UID: NF:commctrl.LoadIconMetric
title: LoadIconMetric function (commctrl.h)
description: Loads a specified icon resource with a client-specified system metric.
helpviewer_keywords: ["LIM_LARGE","LIM_SMALL","LoadIconMetric","LoadIconMetric function [Windows Controls]","_shell_LoadIconMetric","_shell_LoadIconMetric_cpp","commctrl/LoadIconMetric","controls.LoadIconMetric","controls._shell_LoadIconMetric"]
old-location: controls\LoadIconMetric.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\loadiconmetric.htm
ms.date: 12/05/2018
ms.keywords: LIM_LARGE, LIM_SMALL, LoadIconMetric, LoadIconMetric function [Windows Controls], _shell_LoadIconMetric, _shell_LoadIconMetric_cpp, commctrl/LoadIconMetric, controls.LoadIconMetric, controls._shell_LoadIconMetric
req.header: commctrl.h
req.include-header: 
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadIconMetric
 - commctrl/LoadIconMetric
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - LoadIconMetric
---

# LoadIconMetric function


## -description

Loads a specified icon resource with a client-specified system metric.

## -parameters

### -param hinst [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

A handle to the module of either a DLL or executable (.exe) file that contains the icon to be loaded. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlew">GetModuleHandle</a>.

To load a predefined system icon or a standalone icon file, set this parameter to <b>NULL</b>.

### -param pszName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PCWSTR</a></b>

A pointer to a null-terminated, Unicode buffer that contains location information about the icon to load. 

If <i>hinst</i> is non-<b>NULL</b>, <i>pszName</i> specifies the icon resource either by name or ordinal. This ordinal must be packaged by using the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a> macro.

If <i>hinst</i> is <b>NULL</b>, <i>pszName</i> specifies the [identifier (beginning with the IDI\_ prefix)](/windows/win32/menurc/about-icons) of a predefined system icon to load.

### -param lims [in]

Type: <b>int</b>

The desired metric. One of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LIM_SMALL"></a><a id="lim_small"></a><dl>
<dt><b>LIM_SMALL</b></dt>
</dl>
</td>
<td width="60%">
Corresponds to <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">SM_CXSMICON</a>, the recommended pixel width of a small icon.

</td>
</tr>
<tr>
<td width="40%"><a id="LIM_LARGE"></a><a id="lim_large"></a><dl>
<dt><b>LIM_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Corresponds to <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">SM_CXICON</a>, the default pixel width of an icon.

</td>
</tr>
</table>

### -param phico [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a>*</b>

When this function returns, contains a pointer to the handle of the loaded icon.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful, otherwise an error, including the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The contents of the buffer pointed to by <i>pszName</i> do not fit any of the expected interpretations.

</td>
</tr>
</table>

## -remarks

<b>LoadIconMetric</b> is similar to <a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>, but with the capability to specify the icon metric. It is used in place of <b>LoadIcon</b> when the calling application wants to ensure a high quality icon. This is particularly useful in high dots per inch (dpi) situations.

Icons are extracted or created as follows.

<ol>
<li>If an exact size match is found in the resource, that icon is used.</li>
<li>If an exact size match cannot be found and a larger icon is available, a new icon is created by scaling the larger version down to the desired size.</li>
<li>If an exact size match cannot be found and no larger icon is available, a new icon is created by scaling a smaller icon up to the desired size.</li>
</ol>
Comparative calls are shown here for <b>LoadIconMetric</b> and <a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>.

```cpp
NOTIFYICONDATA  nidIconData  = {0};
nidIconData.hIcon = LoadIcon(hInstance, MAKEINTRESOURCE(IDI_ICON));

// Or...

HRESULT hr = LoadIconMetric(hInstance, MAKEINTRESOURCE(IDI_ICON), LIM_SMALL, &nidIconData.hIcon);
```

The application is responsible for calling <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> on the retrieved icon.
