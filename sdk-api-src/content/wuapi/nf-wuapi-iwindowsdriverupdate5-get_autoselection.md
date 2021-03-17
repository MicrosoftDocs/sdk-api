---
UID: NF:wuapi.IWindowsDriverUpdate5.get_AutoSelection
title: IWindowsDriverUpdate5::get_AutoSelection (wuapi.h)
description: Gets an AutoSelectionMode value indicating the automatic selection mode of an update in the Control Panel of Windows Update.
helpviewer_keywords: ["AutoSelection property [Windows Update Agent]","AutoSelection property [Windows Update Agent]","IWindowsDriverUpdate5 interface","IWindowsDriverUpdate5 interface [Windows Update Agent]","AutoSelection property","IWindowsDriverUpdate5.AutoSelection","IWindowsDriverUpdate5.get_AutoSelection","IWindowsDriverUpdate5::AutoSelection","IWindowsDriverUpdate5::get_AutoSelection","get_AutoSelection","wua.iwindowsdriverupdate5_autoselection","wuapi/IWindowsDriverUpdate5::AutoSelection","wuapi/IWindowsDriverUpdate5::get_AutoSelection"]
old-location: wua\iwindowsdriverupdate5_autoselection.htm
tech.root: wua
ms.assetid: 23b7c124-5cb9-4a2d-9f85-d015cfa980ad
ms.date: 12/05/2018
ms.keywords: AutoSelection property [Windows Update Agent], AutoSelection property [Windows Update Agent],IWindowsDriverUpdate5 interface, IWindowsDriverUpdate5 interface [Windows Update Agent],AutoSelection property, IWindowsDriverUpdate5.AutoSelection, IWindowsDriverUpdate5.get_AutoSelection, IWindowsDriverUpdate5::AutoSelection, IWindowsDriverUpdate5::get_AutoSelection, get_AutoSelection, wua.iwindowsdriverupdate5_autoselection, wuapi/IWindowsDriverUpdate5::AutoSelection, wuapi/IWindowsDriverUpdate5::get_AutoSelection
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsDriverUpdate5::get_AutoSelection
 - wuapi/IWindowsDriverUpdate5::get_AutoSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IWindowsDriverUpdate5.AutoSelection
 - IWindowsDriverUpdate5.get_AutoSelection
---

# IWindowsDriverUpdate5::get_AutoSelection


## -description

Gets an <a href="/windows/desktop/api/wuapi/ne-wuapi-autoselectionmode">AutoSelectionMode</a> value indicating the automatic selection mode of an update in the Control Panel of Windows Update.

This property is read-only.

## -parameters

## -remarks

The AutoSelection property indicates whether the update will be automatically selected when the user views the available updates in the Windows Update user interface.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iwindowsdriverupdate5">IWindowsUpdateDriver5</a>