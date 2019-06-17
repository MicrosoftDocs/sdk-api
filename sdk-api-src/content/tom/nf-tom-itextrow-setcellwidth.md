---
UID: NF:tom.ITextRow.SetCellWidth
title: ITextRow::SetCellWidth (tom.h)
author: windows-sdk-content
description: Sets the active cell width in twips.
old-location: controls\itextrow_setcellwidth.htm
tech.root: Controls
ms.assetid: 321c5255-9cd5-46ea-a592-165d288bc452
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellWidth method, ITextRow.SetCellWidth, ITextRow::SetCellWidth, SetCellWidth, SetCellWidth method [Windows Controls], SetCellWidth method [Windows Controls],ITextRow interface, controls.itextrow_setcellwidth, tom/ITextRow::SetCellWidth
ms.topic: method
f1_keywords: ["tom/ITextRow.SetCellWidth"]
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
 - ITextRow.SetCellWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextRow::SetCellWidth


## -description


Sets the active cell width in twips. 


## -parameters




### -param Value [in]

Type: <b>long</b>

The width of the active cell.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The total width of the entire row must be less than 22 inches, or 1440×22.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellwidth">ITextRow::GetCellWidth</a>
 

 

