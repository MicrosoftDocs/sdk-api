---
UID: NF:winuser.GetDialogBaseUnits
title: GetDialogBaseUnits function
author: windows-sdk-content
description: Retrieves the system's dialog base units, which are the average width and height of characters in the system font.
old-location: dlgbox\getdialogbaseunits.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdialogbaseunits.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetDialogBaseUnits, GetDialogBaseUnits function [Dialog Boxes], _win32_GetDialogBaseUnits, _win32_getdialogbaseunits_cpp, dlgbox.getdialogbaseunits, winui._win32_getdialogbaseunits, winuser/GetDialogBaseUnits
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - GetDialogBaseUnits
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetDialogBaseUnits function


## -description


Retrieves the system's dialog base units, which are the average width and height of characters in the system font. For dialog boxes that use the system font, you can use these values to convert between dialog template units, as specified in dialog box templates, and pixels. For dialog boxes that do not use the system font, the conversion from dialog template units to pixels depends on the font used by the dialog box.

For either type of dialog box, it is easier to use the <a href="https://msdn.microsoft.com/20f6477e-d0a3-4781-9f57-0ff05e68c5e6">MapDialogRect</a> function to perform the conversion. <b>MapDialogRect</b> takes the font into account and correctly converts a rectangle from dialog template units into pixels.


## -parameters






## -returns



Type: <b>LONG</b>

The function returns the dialog base units. The low-order word of the return value contains the horizontal dialog box base unit, and the high-order word contains the vertical dialog box base unit. 




## -remarks



The horizontal base unit returned by <b>GetDialogBaseUnits</b> is equal to the average width, in pixels, of the characters in the system font; the vertical base unit is equal to the height, in pixels, of the font.

The system font is used only if the dialog box template fails to specify a font. Most dialog box templates specify a font; as a result, this function is not useful for most dialog boxes.
 

For a dialog box that does not use the system font, the base units are the average width and height, in pixels, of the characters in the dialog's font. You can use the <a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a> and <a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a> functions to calculate these values for a selected font. However, by using the <a href="https://msdn.microsoft.com/20f6477e-d0a3-4781-9f57-0ff05e68c5e6">MapDialogRect</a> function, you can avoid errors that might result if your calculations differ from those performed by the system.

Each horizontal base unit is equal to 4 horizontal dialog template units; each vertical base unit is equal to 8 vertical dialog template units. Therefore, to convert dialog template units to pixels, use the following formulas: 		
				
				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
pixelX = MulDiv(templateunitX, baseunitX, 4);
pixelY = MulDiv(templateunitY, baseunitY, 8);</pre>
</td>
</tr>
</table></span></div>
Similarly, to convert from pixels to dialog template units, use the following formulas:
				
				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
templateunitX = MulDiv(pixelX, 4, baseunitX);
templateunitY = MulDiv(pixelY, 8, baseunitY);</pre>
</td>
</tr>
</table></span></div>

#### Examples


			
			For an example, see "Creating a Combo Box Toolbar" in <a href="_win32_Using_Combo_Boxes">Using Combo Boxes</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/20f6477e-d0a3-4781-9f57-0ff05e68c5e6">MapDialogRect</a>



<b>Reference</b>
 

 

