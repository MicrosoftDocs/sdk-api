---
UID: NS:winddi._FD_KERNINGPAIR
title: "_FD_KERNINGPAIR"
author: windows-driver-content
description: The FD_KERNINGPAIR structure is used to store information about kerning pairs.
old-location: display\fd_kerningpair.htm
old-project: display
ms.assetid: 5c5eced6-a0a3-448e-bcb3-57be1b703797
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: FD_KERNINGPAIR, FD_KERNINGPAIR structure [Display Devices], _FD_KERNINGPAIR, display.fd_kerningpair, grstrcts_5e6126d0-b3c2-4964-ab7a-f3ec90162b7e.xml, winddi/FD_KERNINGPAIR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FD_KERNINGPAIR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	FD_KERNINGPAIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FD_KERNINGPAIR structure


## -description


The FD_KERNINGPAIR structure is used to store information about kerning pairs.


## -struct-fields




### -field wcFirst

Specifies the code point of the first character in the kerning pair.


### -field wcSecond

Specifies the code point of the second character in the kerning pair.


### -field fwdKern

Specifies the kerning value, in font (notional) units, for the kerning pair. If this value is greater than zero, the characters will be moved apart; otherwise, the characters will be moved together. For information about the FWORD data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


## -remarks



An array of FD_KERNINGPAIR structures must be null-terminated, which means the last FD_KERNINGPAIR structure in the array has all structure members set to zero. An array of FD_KERNINGPAIR structures must be sorted in increasing order according to an unsigned 32-bit key, calculated as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>    wcFirst + 65536 * wcSecond.</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556266">DrvQueryFontTree</a>
 

 

