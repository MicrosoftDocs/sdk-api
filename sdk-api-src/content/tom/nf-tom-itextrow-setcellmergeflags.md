---
UID: NF:tom.ITextRow.SetCellMergeFlags
title: ITextRow::SetCellMergeFlags (tom.h)
description: Sets the merge flags of the active cell.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellMergeFlags method","ITextRow.SetCellMergeFlags","ITextRow::SetCellMergeFlags","SetCellMergeFlags","SetCellMergeFlags method [Windows Controls]","SetCellMergeFlags method [Windows Controls]","ITextRow interface","controls.itextrow_setcellmergeflags","tom/ITextRow::SetCellMergeFlags","tomHContCell","tomHStartCell","tomVLowCell","tomVTopCell"]
old-location: controls\itextrow_setcellmergeflags.htm
tech.root: Controls
ms.assetid: a60966cc-03c6-4cb9-b424-eb59f68d1fd1
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellMergeFlags method, ITextRow.SetCellMergeFlags, ITextRow::SetCellMergeFlags, SetCellMergeFlags, SetCellMergeFlags method [Windows Controls], SetCellMergeFlags method [Windows Controls],ITextRow interface, controls.itextrow_setcellmergeflags, tom/ITextRow::SetCellMergeFlags, tomHContCell, tomHStartCell, tomVLowCell, tomVTopCell
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRow::SetCellMergeFlags
 - tom/ITextRow::SetCellMergeFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRow.SetCellMergeFlags
---

# ITextRow::SetCellMergeFlags


## -description

Sets the merge flags of the active cell.

## -parameters

### -param Value [in]

Type: <b>long</b>

The merge flag. It can be one of these values.


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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellmergeflags">ITextRow::GetCellMergeFlags</a>