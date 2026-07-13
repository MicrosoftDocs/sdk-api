---
UID: NF:icm.SetupColorMatchingA
title: SetupColorMatchingA
description: Creates a Color Management dialog box that lets the user choose whether to enable color management and, if so, provides control over the color profiles used and over the [rendering intent](/windows/win32/wcs/r). (ANSI)
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Icmui.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icmui.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - icmui.dll
api_name:
 - SetupColorMatchingA
 - SetupColorMatching
f1_keywords:
 - SetupColorMatchingA
 - icm/SetupColorMatchingA
 - SetupColorMatching
 - icm/SetupColorMatching
dev_langs:
 - c++
---

## -description

Creates a Color Management dialog box that lets the user choose whether to enable color management and, if so, provides control over the color profiles used and over the [rendering intent](/windows/win32/wcs/r).

## -parameters

### -param pcms

Pointer to a [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) structure that on entry contains information used to initialize the dialog box.

When **SetupColorMatching** returns, if the user clicked the OK button, this structure contains information about the user's selection. Otherwise, if an error occurred or the user canceled the dialog box, the structure is left unchanged.

## -returns

If this function succeeds, the return value is **TRUE** indicating that no errors occurred and the user clicked the OK button.

If this function fails, the return value is **FALSE** indicating that an error occurred or the dialog was canceled. For extended error information, call **GetLastError**.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
