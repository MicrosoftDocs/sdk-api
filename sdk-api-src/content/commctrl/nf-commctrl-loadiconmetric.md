---
UID: NF:commctrl.LoadIconMetric
title: LoadIconMetric function
author: windows-sdk-content
description: Loads a specified icon resource with a client-specified system metric.
old-location: controls\LoadIconMetric.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\loadiconmetric.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LIM_LARGE, LIM_SMALL, LoadIconMetric, LoadIconMetric function [Windows Controls], _shell_LoadIconMetric, _shell_LoadIconMetric_cpp, commctrl/LoadIconMetric, controls.LoadIconMetric, controls._shell_LoadIconMetric
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: commctrl.h
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
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - LoadIconMetric
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# LoadIconMetric function


## -description


Loads a specified icon resource with a client-specified system metric.


## -parameters




### -param hinst [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HINSTANCE</a></b>

A handle to the module of either a DLL or executable (.exe) file that contains the icon to be loaded. For more information, see <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>.

                    

To load a predefined icon or a standalone icon file, set this parameter to <b>NULL</b>.


### -param pszName [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">PCWSTR</a></b>

A pointer to a null-terminated, Unicode buffer that contains location information about the icon to load. It is interpreted as follows:
        
                    

If <i>hinst</i> is <b>NULL</b>, <i>pszName</i> can specify one of two things.

<ol>
<li>The identifier of a predefined icon to load. These identifiers are recognized.

                            <ul>
<li>IDI_APPLICATION</li>
<li>IDI_INFORMATION</li>
<li>IDI_ERROR</li>
<li>IDI_WARNING</li>
<li>IDI_SHIELD</li>
<li>IDI_QUESTION</li>
</ul>
To pass these constants to the <b>LoadIconMetric</b> function, use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro. For example, to load the IDI_ERROR icon, pass <code>MAKEINTRESOURCE(IDI_ERROR)</code> as the <i>pszName</i> parameter and <b>NULL</b> as the <i>hinst</i> parameter.

</li>
<li>The name of a standalone icon (.ico) file.</li>
</ol>
If <i>hinst</i> is non-null, <i>pszName</i> can specify one of two things.

<ol>
<li>The name of the icon resource, if the icon resource is to be loaded by name from the module.</li>
<li>The icon ordinal, if the icon resource is to be loaded by ordinal from the module. This ordinal must be packaged by using the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro.</li>
</ol>

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
Corresponds to <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">SM_CXSMICON</a>, the recommended pixel width of a small icon.

</td>
</tr>
<tr>
<td width="40%"><a id="LIM_LARGE"></a><a id="lim_large"></a><dl>
<dt><b>LIM_LARGE</b></dt>
</dl>
</td>
<td width="60%">
Corresponds to<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">SM_CXICON</a>, the default pixel width of an icon.

</td>
</tr>
</table>
 


### -param phico [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HICON</a>*</b>

When this function returns, contains a pointer to the handle of the loaded icon.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

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



<b>LoadIconMetric</b> is similar to <a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a>, but with the capability to specify the icon metric. It is used in place of <b>LoadIcon</b> when the calling application wants to ensure a high quality icon. This is particularly useful in high dots per inch (dpi) situations.

Icons are extracted or created as follows.

                

<ol>
<li>If an exact size match is found in the resource, that icon is used.</li>
<li>If an exact size match cannot be found and a larger icon is available, a new icon is created by scaling the larger version down to the desired size.</li>
<li>If an exact size match cannot be found and no larger icon is available, a new icon is created by scaling a smaller icon up to the desired size.</li>
</ol>
Comparative calls are shown here for <b>LoadIconMetric</b> and <a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a>.

<pre class="syntax" xml:space="preserve"><code>NOTIFYICONDATA  nidIconData  = {0};
nidIconData.hIcon = LoadIcon(hInstance, MAKEINTRESOURCE(IDI_ICON));

// Or...

HRESULT hr = LoadIconMetric(hInstance, MAKEINTRESOURCE(IDI_ICON), LIM_SMALL, &amp;nidIconData.hIcon);</code></pre>
The application is responsible for calling <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a> on the retrieved icon.



