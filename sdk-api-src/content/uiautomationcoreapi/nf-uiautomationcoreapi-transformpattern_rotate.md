---
UID: NF:uiautomationcoreapi.TransformPattern_Rotate
title: TransformPattern_Rotate function (uiautomationcoreapi.h)
description: Rotates an element on the screen.
helpviewer_keywords: ["TransformPattern_Rotate","TransformPattern_Rotate function [Windows Accessibility]","uiauto.uiauto_TransformPattern_RotateConPat","uiauto_TransformPattern_RotateConPat","uiautomationcoreapi/TransformPattern_Rotate","winauto.uiauto_TransformPattern_RotateConPat"]
old-location: winauto\uiauto_TransformPattern_RotateConPat.htm
tech.root: WinAuto
ms.assetid: c3c61c67-7c4a-4211-90f9-b5000a4938a3
ms.date: 12/05/2018
ms.keywords: TransformPattern_Rotate, TransformPattern_Rotate function [Windows Accessibility], uiauto.uiauto_TransformPattern_RotateConPat, uiauto_TransformPattern_RotateConPat, uiautomationcoreapi/TransformPattern_Rotate, winauto.uiauto_TransformPattern_RotateConPat
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TransformPattern_Rotate
 - uiautomationcoreapi/TransformPattern_Rotate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - TransformPattern_Rotate
---

# TransformPattern_Rotate function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Rotates an element on the screen.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

### -param degrees [in]

Type: <b>double</b>

The number of degrees to rotate the control. 
				Positive values are clockwise; negative values are counterclockwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.