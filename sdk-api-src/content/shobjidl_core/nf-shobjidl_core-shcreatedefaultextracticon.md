---
UID: NF:shobjidl_core.SHCreateDefaultExtractIcon
title: SHCreateDefaultExtractIcon function
author: windows-sdk-content
description: Creates a standard icon extractor, whose defaults can be further configured via the IDefaultExtractIconInit interface.
old-location: shell\SHCreateDefaultExtractIcon.htm
tech.root: shell
ms.assetid: 483dc9ae-4820-47f1-888e-ad7a6bdf3d29
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: SHCreateDefaultExtractIcon, SHCreateDefaultExtractIcon function [Windows Shell], _shell_SHCreateDefaultExtractIcon, shell.SHCreateDefaultExtractIcon, shobjidl_core/SHCreateDefaultExtractIcon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHCreateDefaultExtractIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateDefaultExtractIcon function


## -description


Creates a standard icon extractor, whose defaults can be further configured via the <a href="https://msdn.microsoft.com/27b952e3-f17a-4844-8c39-2ae240179d02">IDefaultExtractIconInit</a> interface.


## -parameters




### -param riid

Type: <b>REFIID</b>

A reference to interface ID.


### -param ppv [out]

Type: <b>void**</b>

The address of <a href="https://msdn.microsoft.com/27b952e3-f17a-4844-8c39-2ae240179d02">IDefaultExtractIconInit</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The intended usage for this function is as follows:
            
                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IExtractIcon *pxi;

IDefaultExtractIconInit *pdxi;

HRESULT hr = SHCreateDefaultExtractIcon(IID_PPV_ARGS(&amp;pdxi);

 if (SUCCEEDED(hr)) &amp;&amp;

      SUCCEEDED(hr = pdxi-&gt;SetFlags(GIL_PERCLASS)) &amp;&amp;

      SUCCEEDED(hr = pdxi-&gt;SetKey(hkey)) &amp;&amp;   // optional

      SUCCEEDED(hr = pdxi-&gt;SetNormalIcon(L"this.dll", 1)) &amp;&amp;

      SUCCEEDED(hr = pdxi-&gt;SetOpenIcon(NULL, SIID_FOLDEROPEN)) &amp;&amp; // optional

      SUCCEEDED(hr = pdxi-&gt;SetDefaultIcon(NULL, SIID_FOLDER)) &amp;&amp; // optional

      SUCCEEDED(hr = pdxi-&gt;SetShortcutIcon(L"this.dll", 2))) // optional

{

      hr = pdxi-&gt;QueryInterface(IID_PPV_ARGS(&amp;pxi)) 

}

 if (pdxi)

{

    pdxi-&gt;Release();

}</pre>
</td>
</tr>
</table></span></div>


