---
UID: NF:shobjidl_core.IShellIconOverlayIdentifier.GetPriority
title: IShellIconOverlayIdentifier::GetPriority (shobjidl_core.h)
description: Specifies the priority of an icon overlay.
helpviewer_keywords: ["GetPriority","GetPriority method [Windows Shell]","GetPriority method [Windows Shell]","IShellIconOverlayIdentifier interface","IShellIconOverlayIdentifier interface [Windows Shell]","GetPriority method","IShellIconOverlayIdentifier.GetPriority","IShellIconOverlayIdentifier::GetPriority","_win32_IShellIconOverlayIdentifier_GetPriority","shell.IShellIconOverlayIdentifier_GetPriority","shobjidl_core/IShellIconOverlayIdentifier::GetPriority"]
old-location: shell\IShellIconOverlayIdentifier_GetPriority.htm
tech.root: shell
ms.assetid: c191bcf7-8b49-4276-9e30-2a8dcaf1fc46
ms.date: 12/05/2018
ms.keywords: GetPriority, GetPriority method [Windows Shell], GetPriority method [Windows Shell],IShellIconOverlayIdentifier interface, IShellIconOverlayIdentifier interface [Windows Shell],GetPriority method, IShellIconOverlayIdentifier.GetPriority, IShellIconOverlayIdentifier::GetPriority, _win32_IShellIconOverlayIdentifier_GetPriority, shell.IShellIconOverlayIdentifier_GetPriority, shobjidl_core/IShellIconOverlayIdentifier::GetPriority
req.header: shobjidl_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellIconOverlayIdentifier::GetPriority
 - shobjidl_core/IShellIconOverlayIdentifier::GetPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlayIdentifier.GetPriority
---

# IShellIconOverlayIdentifier::GetPriority


## -description

Specifies the priority of an icon overlay.

## -parameters

### -param pPriority [out]

Type: <b>int*</b>

The address of a value that indicates the priority of the overlay identifier. Possible values range from zero to 100, with zero the highest priority.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.

## -remarks

If more than one icon overlay is available for an object, the one with highest priority is chosen. The Shell has a set of internal rules that determine priority for many cases. The value returned by <b>GetPriority</b> is used for those cases in which the Shell's internal rules do not apply. Typically, you should set the value to zero. However, the priority value is useful when you have implemented two or more icon overlay handlers that can request icon overlay icons for the same object. By setting the priority values appropriately, you can specify which of the requested icon overlays will be displayed.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier">IShellIconOverlayIdentifier</a>