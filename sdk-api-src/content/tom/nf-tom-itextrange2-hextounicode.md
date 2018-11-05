---
UID: NF:tom.ITextRange2.HexToUnicode
title: ITextRange2::HexToUnicode
author: windows-sdk-content
description: Converts and replaces the hexadecimal number at the end of this range to a Unicode character.
old-location: controls\itextrange2_hextounicode.htm
tech.root: controls
ms.assetid: 024f9f32-2362-4f1c-b8db-9b4fb1ee157c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: HexToUnicode, HexToUnicode method [Windows Controls], HexToUnicode method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],HexToUnicode method, ITextRange2.HexToUnicode, ITextRange2::HexToUnicode, controls.itextrange2_hextounicode, tom/ITextRange2::HexToUnicode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.HexToUnicode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::HexToUnicode


## -description


Converts and replaces the hexadecimal number at the end of this range to a Unicode character.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Some Unicode surrogates for hex values from 0x10000 up to 0x10FFFF are for internal use:<table>
<tr>
<th>Hex values</th>
<th>Available for use</th>
</tr>
<tr>
<td>7, 0xFDD0 — 0xFDEF, 0xFFF9 — 0xFFFF</td>
<td>Internal use only</td>
</tr>
<tr>
<td>0xA — 0xD in the C0 range (0-0x1F)</td>
<td>Available for use</td>
</tr>
<tr>
<td>C1 range (0x80 — 0x9F)</td>
<td>Internal use only</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

