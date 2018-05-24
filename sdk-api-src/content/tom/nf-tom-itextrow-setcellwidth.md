---
UID: NF:tom.ITextRow.SetCellWidth
title: ITextRow::SetCellWidth
author: windows-driver-content
description: Sets the active cell width in twips.
old-location: controls\itextrow_setcellwidth.htm
old-project: Controls
ms.assetid: 321c5255-9cd5-46ea-a592-165d288bc452
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellWidth method, ITextRow.SetCellWidth, ITextRow::SetCellWidth, SetCellWidth, SetCellWidth method [Windows Controls], SetCellWidth method [Windows Controls],ITextRow interface, controls.itextrow_setcellwidth, tom/ITextRow::SetCellWidth
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRow.SetCellWidth
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::SetCellWidth


## -description


Sets the active cell width in twips. 


## -parameters




### -param Value [in]

Type: <b>long</b>

The width of the active cell.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The total width of the entire row must be less than 22 inches, or 1440×22.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/dc73fdf4-29ce-4432-825d-725d61717b7a">ITextRow::GetCellWidth</a>
 

 

