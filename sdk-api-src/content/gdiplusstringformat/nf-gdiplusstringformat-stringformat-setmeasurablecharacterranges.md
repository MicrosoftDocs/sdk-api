---
UID: NF:gdiplusstringformat.StringFormat.SetMeasurableCharacterRanges
title: StringFormat::SetMeasurableCharacterRanges
author: windows-sdk-content
description: The StringFormat::SetMeasurableCharacterRanges method sets a series of character ranges for this StringFormat object that, when in a string, can be measured by the MeasureCharacterRanges method.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setmeasurablecharacterranges.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SetMeasurableCharacterRanges, SetMeasurableCharacterRanges method [GDI+], SetMeasurableCharacterRanges method [GDI+],StringFormat class, StringFormat class [GDI+],SetMeasurableCharacterRanges method, StringFormat.SetMeasurableCharacterRanges, StringFormat::SetMeasurableCharacterRanges, _gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_, gdiplus._gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusstringformat.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	StringFormat.SetMeasurableCharacterRanges
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# StringFormat::SetMeasurableCharacterRanges


## -description


The <b>StringFormat::SetMeasurableCharacterRanges</b> method sets a series of character ranges for this 
			<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object that, when in a string, can be measured by the <a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a> method.


## -parameters




### -param rangeCount [in]

Type: <b>INT</b>

Integer that specifies the number of character ranges in the 
					<i>ranges</i> array. 


### -param ranges [in]

Type: <b>const <a href="https://msdn.microsoft.com/7bb98500-d1cf-422d-b1ff-a7ca4c84560e">CharacterRange</a>*</b>

Pointer to an array of 
					<a href="https://msdn.microsoft.com/7bb98500-d1cf-422d-b1ff-a7ca4c84560e">CharacterRange</a> objects that specify the character ranges to be measured. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/2176e638-5d83-46ae-ab4f-a3031d46bde2">MeasureCharacterRanges</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>



<a href="https://msdn.microsoft.com/374b89d4-4f6f-4875-a34f-8a6e9ee379ab">StringFormat::GetMeasurableCharacterRangeCount</a>
 

 

