---
UID: NF:shlwapi.SHGetInverseCMAP
title: SHGetInverseCMAP function (shlwapi.h)
description: Retrieves the inverse color table mapping for the halftone palette.
helpviewer_keywords: ["SHGetInverseCMAP","SHGetInverseCMAP function [Windows Shell]","_shell_SHGetInverseCMAP","shell.SHGetInverseCMAP","shlwapi/SHGetInverseCMAP"]
old-location: shell\SHGetInverseCMAP.htm
tech.root: shell
ms.assetid: 46d5ccd2-3c5d-431b-b27b-6a7a95043e0a
ms.date: 12/05/2018
ms.keywords: SHGetInverseCMAP, SHGetInverseCMAP function [Windows Shell], _shell_SHGetInverseCMAP, shell.SHGetInverseCMAP, shlwapi/SHGetInverseCMAP
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetInverseCMAP
 - shlwapi/SHGetInverseCMAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
 - SHGetInverseCMAP
---

# SHGetInverseCMAP function


## -description

<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Retrieves the inverse color table mapping for the halftone palette.

## -parameters

### -param pbMap [out]

Type: <b>BYTE*</b>

A pointer to an array of <b>BYTE</b><b>s</b> that receives the inverse color table mapping, or a pointer to an <b>LPBYTE</b> which receives a pointer to a cached copy of the inverse color table mapping, depending on the value of the <i>cbMap</i> parameter.

### -param cbMap [in]

Type: <b>ULONG</b>

The size of the buffer pointed to by <i>pbMap</i>, which also defines its contents. Two values are recognized.



#### (sizeof(BYTE*))

The buffer pointed to by <i>pbMap</i> receives a pointer to a cached copy of the inverse color map table.



#### (32768)

The buffer pointed to by <i>pbMap</i> receives a copy of the inverse color map table. The buffer must be exactly 32,768 bytes in size.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The inverse color mapping table is a table of 32,768 bytes. It contains the indexes of colors in the halftone palette. Each index is stored at a position in the buffer that corresponds to a particular RGB value expressed in 555 format. These pairings allow you to find a color in the halftone palette which is a close approximation of the original color.
                
                

For example, the method for determining a color in the halftone palette that is a close approximation for the color #306040 is as follows:

<ol>
<li>Decompose the color into its red, green, and blue components. In this case, the red component is 0x30, the green component is 0x60 and the blue component is 0x40.</li>
<li>Reassemble the color into 555 format. The formula for reducing a 24-bit RGB color into 555 format is shown here.

                        


```
((red / 8) << 10) + ((blue / 8) << 5) + (green / 8)
```


In this example, the value in 555 format is ((0x30 / 8) &lt;&lt; 10) + ((0x60 / 8) &lt;&lt; 5) + (0x40 / 8) = 6536.

</li>
<li>The index value stored in position 6536 in the inverse color map table is the index of the color in the halftone palette that is a reasonable approximation to the color #306040.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createhalftonepalette">CreateHalftonePalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getnearestcolor">GetNearestColor</a>