---
UID: NE:wuapi.tagAutoSelectionMode
title: AutoSelectionMode (wuapi.h)
description: Defines the types of logic that is used to determine whether a particular update will be automatically selected when the user views available updates in the Windows Update user interface.
helpviewer_keywords: ["AutoSelectionMode","AutoSelectionMode enumeration [Windows Update Agent]","asAlwaysAutoSelect","asAutoSelectIfDownloaded","asLetWindowsUpdateDecide","asNeverAutoSelect","wua.autoselectionmode","wuapi/AutoSelectionMode","wuapi/asAlwaysAutoSelect","wuapi/asAutoSelectIfDownloaded","wuapi/asLetWindowsUpdateDecide","wuapi/asNeverAutoSelect"]
old-location: wua\autoselectionmode.htm
tech.root: wua
ms.assetid: 847fd8a3-eb00-43f7-a89f-579cd79d0620
ms.date: 12/05/2018
ms.keywords: AutoSelectionMode, AutoSelectionMode enumeration [Windows Update Agent], asAlwaysAutoSelect, asAutoSelectIfDownloaded, asLetWindowsUpdateDecide, asNeverAutoSelect, wua.autoselectionmode, wuapi/AutoSelectionMode, wuapi/asAlwaysAutoSelect, wuapi/asAutoSelectIfDownloaded, wuapi/asLetWindowsUpdateDecide, wuapi/asNeverAutoSelect
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AutoSelectionMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAutoSelectionMode
 - wuapi/tagAutoSelectionMode
 - AutoSelectionMode
 - wuapi/AutoSelectionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - AutoSelectionMode
---

# AutoSelectionMode enumeration


## -description

Defines  the types of logic that is used to determine whether a particular update will be automatically selected when the user views  available updates in the Windows Update user interface.

## -enum-fields

### -field asLetWindowsUpdateDecide:0

Use the standard logic. The update will be automatically selected if it is important, or if it is recommended and Windows Update has been configured to treat recommended updates as important. Otherwise, the update will not be automatically selected.

### -field asAutoSelectIfDownloaded:1

The update will be automatically selected only if it has been completely downloaded.

### -field asNeverAutoSelect:2

The update will never be automatically selected.

### -field asAlwaysAutoSelect:3

The update will always be automatically selected.

## -remarks

In versions of the Windows Update Agent (WUA) in which <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate5">IUpdate5</a> is not available, all updates are processed by using the standard logic.
