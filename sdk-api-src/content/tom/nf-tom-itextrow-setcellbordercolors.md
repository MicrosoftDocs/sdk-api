---
UID: NF:tom.ITextRow.SetCellBorderColors
title: ITextRow::SetCellBorderColors
author: windows-sdk-content
description: Sets the border colors of the active cell.
old-location: controls\itextrow_setcellbordercolors.htm
old-project: Controls
ms.assetid: 2a8762ba-a92b-46aa-99bc-57406a872174
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellBorderColors method, ITextRow.SetCellBorderColors, ITextRow::SetCellBorderColors, SetCellBorderColors, SetCellBorderColors method [Windows Controls], SetCellBorderColors method [Windows Controls],ITextRow interface, controls.itextrow_setcellbordercolors, tom/ITextRow::SetCellBorderColors
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRow.SetCellBorderColors
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::SetCellBorderColors


## -description


Sets the border colors of the active cell.


## -parameters




### -param crLeft [in]

Type: <b>long</b>

The left border color.


### -param crTop [in]

Type: <b>long</b>

The top border color.


### -param crRight [in]

Type: <b>long</b>

The right border color.


### -param crBottom [in]

Type: <b>long</b>

The bottom border color.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/2cc0a3b0-3988-4dff-9553-a86d37f4011f">ITextRow::GetCellBorderColors</a>
 

 

