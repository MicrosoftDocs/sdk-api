---
UID: NF:uiautomationcoreapi.UiaRectIsEmpty
title: UiaRectIsEmpty function (uiautomationcoreapi.h)
description: Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.
helpviewer_keywords: ["UiaRectIsEmpty","UiaRectIsEmpty function [Windows Accessibility]","uiauto.uiauto_UiaRectIsEmptyFunction","uiauto_UiaRectIsEmptyFunction","uiautomationcoreapi/UiaRectIsEmpty","winauto.uiauto_UiaRectIsEmptyFunction"]
old-location: winauto\uiauto_UiaRectIsEmptyFunction.htm
tech.root: WinAuto
ms.assetid: a1bcf983-a40c-4a9f-95f8-3124d62e07a3
ms.date: 12/05/2018
ms.keywords: UiaRectIsEmpty, UiaRectIsEmpty function [Windows Accessibility], uiauto.uiauto_UiaRectIsEmptyFunction, uiauto_UiaRectIsEmptyFunction, uiautomationcoreapi/UiaRectIsEmpty, winauto.uiauto_UiaRectIsEmptyFunction
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
 - UiaRectIsEmpty
 - uiautomationcoreapi/UiaRectIsEmpty
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
 - UiaRectIsEmpty
---

# UiaRectIsEmpty function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.

## -parameters

### -param rc [in, ref]

Type: <b>const <a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiarect">UiaRect</a></b>

A reference to a <a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiarect">UiaRect</a> structure that contains the coordinates of the rectangle.

## -returns

Type: <b>bool</b>

<b>TRUE</b> if the rectangle is empty; otherwise <b>FALSE</b>.