---
UID: NF:tom.ITextRow.SetCellBorderWidths
title: ITextRow::SetCellBorderWidths
author: windows-driver-content
description: Sets the border widths of the active cell.
old-location: controls\itextrow_setcellborderwidths.htm
old-project: Controls
ms.assetid: 343270e6-8f92-4429-9350-4031ae8bb0e0
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellBorderWidths method, ITextRow.SetCellBorderWidths, ITextRow::SetCellBorderWidths, SetCellBorderWidths, SetCellBorderWidths method [Windows Controls], SetCellBorderWidths method [Windows Controls],ITextRow interface, controls.itextrow_setcellborderwidths, tom/ITextRow::SetCellBorderWidths
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
-	ITextRow.SetCellBorderWidths
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::SetCellBorderWidths


## -description


Sets the border widths of the active cell.


## -parameters




### -param duLeft [in]

Type: <b>long</b>

The left border width.


### -param duTop [in]

Type: <b>long</b>

The top border width.


### -param duRight [in]

Type: <b>long</b>

The right border width.


### -param duBottom [in]

Type: <b>long</b>

The bottom border width.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/e0ab26ca-ffb6-4f75-846b-e267e4ad6572">ITextRow::GetCellBorderWidths</a>
 

 

