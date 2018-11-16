---
UID: NS:imm.tagCOMPOSITIONFORM
title: tagCOMPOSITIONFORM
author: windows-sdk-content
description: Contains style and position information for a composition window.
old-location: intl\compositionform.htm
tech.root: Intl
ms.assetid: 9b76474a-1ea9-4fcf-9fa8-deee5009a7ba
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPCOMPOSITIONFORM, *NPCOMPOSITIONFORM, *PCOMPOSITIONFORM, COMPOSITIONFORM, COMPOSITIONFORM structure [Internationalization for Windows Applications], PCOMPOSITIONFORM, PCOMPOSITIONFORM structure pointer [Internationalization for Windows Applications], _win32_COMPOSITIONFORM_str, imm/COMPOSITIONFORM, imm/PCOMPOSITIONFORM, intl.compositionform, tagCOMPOSITIONFORM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: imm.h
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
 - Imm.h
api_name:
 - COMPOSITIONFORM
product: Windows
targetos: Windows
req.typenames: COMPOSITIONFORM, *PCOMPOSITIONFORM, *NPCOMPOSITIONFORM, *LPCOMPOSITIONFORM
req.redist: 
---

# tagCOMPOSITIONFORM structure


## -description



Contains style and position information for a composition window.




## -struct-fields




### -field dwStyle

Position style. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CFS_DEFAULT</td>
<td>Move the composition window to the default position. The IME window can display the composition window outside the client area, such as in a floating window.</td>
</tr>
<tr>
<td>CFS_FORCE_POSITION</td>
<td>Display the upper left corner of the composition window at exactly the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the composition window and are not subject to adjustment by the IME.</td>
</tr>
<tr>
<td>CFS_POINT</td>
<td>Display the upper left corner of the composition window at the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the composition window and are subject to adjustment by the IME.</td>
</tr>
<tr>
<td>CFS_RECT</td>
<td>Display the composition window at the position specified by <b>rcArea</b>. The coordinates are relative to the upper left of the window containing the composition window.</td>
</tr>
</table>
 


### -field ptCurrentPos

A <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure containing the coordinates of the upper left corner of the composition window.


### -field rcArea

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure containing the coordinates of the upper left and lower right corners of the composition window.


## -remarks



Some IME windows adjust the composition window position specified by the system or the application. The CFS_FORCE_POSITION directs the IME window to skip this adjustment.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

