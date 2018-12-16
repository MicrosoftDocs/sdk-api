---
UID: NF:tom.ITextRow.SetCellIndex
title: ITextRow::SetCellIndex
author: windows-sdk-content
description: Sets the index of the active cell.
old-location: controls\itextrow_setcellindex.htm
tech.root: controls
ms.assetid: 4b31ed10-f153-4614-ba96-95271fe4b218
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellIndex method, ITextRow.SetCellIndex, ITextRow::SetCellIndex, SetCellIndex, SetCellIndex method [Windows Controls], SetCellIndex method [Windows Controls],ITextRow interface, controls.itextrow_setcellindex, tom/ITextRow::SetCellIndex
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
 - ITextRow.SetCellIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::SetCellIndex


## -description


Sets the index of the active cell.


## -parameters




### -param Value [in]

Type: <b>long</b>

The cell index.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



You can get or set parameters for an active cell.

 If the cell index is greater than the cell count, and the cell index is less that 63 (the maximum cell count), then the cell count is increased to cell index + 1.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/4aae4fe5-5a54-4f32-9f89-01752701c871">ITextRow::GetCellCount</a>



<a href="https://msdn.microsoft.com/7768e073-929c-43a4-8c4f-a67f89a0e7ee">ITextRow::GetCellIndex</a>



<a href="https://msdn.microsoft.com/a2e1436a-ef36-41cd-9ea1-fb7abfad7631">ITextRow::SetCellCount</a>
 

 

