---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITextRange2::UnicodeToHex


## -description


Converts the Unicode character(s) preceding the start position of this text range to a hexadecimal number, and selects it.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Some Unicode surrogates for hex values from 0x10000 up to 0x10FFFF are for internal use: <table>
<tr>
<th>Hex values</th>
<th>Available for use</th>
</tr>
<tr>
<td> 0xFDD0 – 0xFDEF, 0xFFF9-0xFFFF</td>
<td>Internal use only</td>
</tr>
<tr>
<td>0xA – 0xD in the C0 range (0-0x1F)</td>
<td>Available for use</td>
</tr>
<tr>
<td>C1 range (0x80 – 0x9F)</td>
<td>Internal use only</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

