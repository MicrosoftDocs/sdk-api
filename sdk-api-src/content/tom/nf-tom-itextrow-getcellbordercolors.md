---
UID: NF:tom.ITextRow.GetCellBorderColors
title: ITextRow::GetCellBorderColors
author: windows-sdk-content
description: Gets the border colors of the active cell.
old-location: controls\itextrow_getcellbordercolors.htm
tech.root: controls
ms.assetid: 2cc0a3b0-3988-4dff-9553-a86d37f4011f
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetCellBorderColors, GetCellBorderColors method [Windows Controls], GetCellBorderColors method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellBorderColors method, ITextRow.GetCellBorderColors, ITextRow::GetCellBorderColors, controls.itextrow_getcellbordercolors, tom/ITextRow::GetCellBorderColors
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
 - ITextRow.GetCellBorderColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::GetCellBorderColors


## -description


Gets the border colors of the active cell.


## -parameters




### -param pcrLeft [in]

Type: <b>long*</b>

The active-cell left border color.


### -param pcrTop [in]

Type: <b>long*</b>

The active-cell top border color.


### -param pcrRight [in]

Type: <b>long*</b>

The active-cell right border color.


### -param pcrBottom [in]

Type: <b>long*</b>

The active-cell bottom border color.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/2a8762ba-a92b-46aa-99bc-57406a872174">ITextRow::SetCellBorderColors</a>
 

 

