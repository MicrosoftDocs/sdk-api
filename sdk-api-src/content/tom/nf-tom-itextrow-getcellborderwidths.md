---
UID: NF:tom.ITextRow.GetCellBorderWidths
title: ITextRow::GetCellBorderWidths
author: windows-sdk-content
description: Gets the border widths of the active cell.
old-location: controls\itextrow_getcellborderwidths.htm
tech.root: controls
ms.assetid: e0ab26ca-ffb6-4f75-846b-e267e4ad6572
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetCellBorderWidths, GetCellBorderWidths method [Windows Controls], GetCellBorderWidths method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellBorderWidths method, ITextRow.GetCellBorderWidths, ITextRow::GetCellBorderWidths, controls.itextrow_getcellborderwidths, tom/ITextRow::GetCellBorderWidths
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
 - ITextRow.GetCellBorderWidths
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::GetCellBorderWidths


## -description


Gets the border widths of the active cell.


## -parameters




### -param pduLeft [in]

Type: <b>long*</b>

The active-cell left border width.


### -param pduTop [in]

Type: <b>long*</b>

The active-cell top border width.


### -param pduRight [in]

Type: <b>long*</b>

The active-cell right border width.


### -param pduBottom [in]

Type: <b>long*</b>

The active-cell bottom border width.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/343270e6-8f92-4429-9350-4031ae8bb0e0">ITextRow::SetCellBorderWidths</a>
 

 

