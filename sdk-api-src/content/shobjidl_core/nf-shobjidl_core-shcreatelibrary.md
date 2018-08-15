---
UID: NF:shobjidl_core.SHCreateLibrary
title: SHCreateLibrary function
author: windows-sdk-content
description: Creates an IShellLibrary object.
old-location: shell\SHCreateLibrary.htm
old-project: shell
ms.assetid: 7e682a2e-5140-49ad-88de-ac681025aca4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHCreateLibrary, SHCreateLibrary function [Windows Shell], _shell_SHCreateLibrary, shell.SHCreateLibrary, shobjidl_core/SHCreateLibrary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHCreateLibrary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SHCreateLibrary function


## -description


Creates an <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The IID for <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>. (See usage remarks.)


### -param ppv [out]

Type: <b>void**</b>

Receives a new <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object. (See usage remarks.)


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<h3><a id="Usage"></a><a id="usage"></a><a id="USAGE"></a>Usage</h3>
The <b>IID_PPV_ARGS</b> macro is generally used to generate the <i>riid</i> and <i>ppv</i> parameters for this function. For example:
            
                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#include "shobjidl.h"
#include "objbase.h" // Defines the IID_PPV_ARGS macro.        

...

IShellLibrary *pIShellLib;
SHCreateLibrary(IID_PPV_ARGS(&amp;pIShellLib));
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>
 

 

