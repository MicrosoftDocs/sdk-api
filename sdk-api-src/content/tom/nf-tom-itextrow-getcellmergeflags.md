---
UID: NF:tom.ITextRow.GetCellMergeFlags
title: ITextRow::GetCellMergeFlags
author: windows-driver-content
description: Gets the merge flags of the active cell.
old-location: controls\itextrow_getcellmergeflags.htm
old-project: Controls
ms.assetid: 0e3c0cf4-b371-4622-a183-61d213fc9291
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetCellMergeFlags, GetCellMergeFlags method [Windows Controls], GetCellMergeFlags method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellMergeFlags method, ITextRow.GetCellMergeFlags, ITextRow::GetCellMergeFlags, controls.itextrow_getcellmergeflags, tom/ITextRow::GetCellMergeFlags, tomHContCell, tomHStartCell, tomVLowCell, tomVTopCell
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
-	ITextRow.GetCellMergeFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::GetCellMergeFlags


## -description


Gets the merge flags of the active cell.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The merge flag of the active cell. The flag can be one of the following:

<a id="tomHContCell"></a>
<a id="tomhcontcell"></a>
<a id="TOMHCONTCELL"></a>


#### tomHContCell

<a id="tomHStartCell"></a>
<a id="tomhstartcell"></a>
<a id="TOMHSTARTCELL"></a>


#### tomHStartCell

<a id="tomVLowCell"></a>
<a id="tomvlowcell"></a>
<a id="TOMVLOWCELL"></a>


#### tomVLowCell

<a id="tomVTopCell"></a>
<a id="tomvtopcell"></a>
<a id="TOMVTOPCELL"></a>


#### tomVTopCell


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/a60966cc-03c6-4cb9-b424-eb59f68d1fd1">ITextRow::SetCellMergeFlags</a>
 

 

