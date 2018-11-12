---
UID: NF:vfw.mmioFOURCC
title: mmioFOURCC macro
author: windows-sdk-content
description: The mmioFOURCC macro converts four characters into a four-character code.
old-location: multimedia\mmiofourcc.htm
tech.root: Multimedia
ms.assetid: 616c3b43-9305-49c1-bc46-2e1256647c7d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_win32_mmioFOURCC, mmioFOURCC, mmioFOURCC macro [Windows Multimedia], multimedia.mmiofourcc, vfw/mmioFOURCC"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vfw.h
api_name:
 - mmioFOURCC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mmioFOURCC macro


## -description



The <b>mmioFOURCC</b> macro converts four characters into a four-character code.




## -parameters




### -param ch0

First character of the four-character code. 


### -param ch1

Second character of the four-character code. 


### -param ch2

Third character of the four-character code. 


### -param ch3

Fourth character of the four-character code. 


## -remarks



This macro does not check whether the four-character code it returns is valid.

The <b>mmioFOURCC</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define mmioFOURCC(ch0, ch1, ch2, ch3) \ 
    MAKEFOURCC(ch0, ch1, ch2, ch3); 
 
</pre>
</td>
</tr>
</table></span></div>
The <b>MAKEFOURCC</b> macro, in turn, is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define MAKEFOURCC(ch0, ch1, ch2, ch3)  \ 
    ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) &lt;&lt; 8) |  \ 
    ((DWORD)(BYTE)(ch2) &lt;&lt; 16) | ((DWORD)(BYTE)(ch3) &lt;&lt; 24 )); 
</pre>
</td>
</tr>
</table></span></div>


