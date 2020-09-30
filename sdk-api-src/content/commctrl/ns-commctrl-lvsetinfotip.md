---
UID: NS:commctrl.tagLVSETINFOTIP
title: LVSETINFOTIP (commctrl.h)
description: Provides information about tooltip text that is to be set.
helpviewer_keywords: ["*PLVSETINFOTIP","LVSETINFOTIP","LVSETINFOTIP structure [Windows Controls]","PLVSETINFOTIP","PLVSETINFOTIP structure pointer [Windows Controls]","commctrl/LVSETINFOTIP","commctrl/PLVSETINFOTIP","controls.LVSETINFOTIP","controls.inet_LVSETINFOTIP","inet_LVSETINFOTIP","inet_LVSETINFOTIP_cpp"]
old-location: controls\LVSETINFOTIP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvsetinfotip.htm
ms.date: 12/05/2018
ms.keywords: '*PLVSETINFOTIP, LVSETINFOTIP, LVSETINFOTIP structure [Windows Controls], PLVSETINFOTIP, PLVSETINFOTIP structure pointer [Windows Controls], commctrl/LVSETINFOTIP, commctrl/PLVSETINFOTIP, controls.LVSETINFOTIP, controls.inet_LVSETINFOTIP, inet_LVSETINFOTIP, inet_LVSETINFOTIP_cpp'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LVSETINFOTIP, *PLVSETINFOTIP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVSETINFOTIP
 - commctrl/tagLVSETINFOTIP
 - PLVSETINFOTIP
 - commctrl/PLVSETINFOTIP
 - LVSETINFOTIP
 - commctrl/LVSETINFOTIP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - LVSETINFOTIP
---

# LVSETINFOTIP structure


## -description

Provides information about tooltip text that is to be set.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the <b>LVSETINFOTIP</b> structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flag that specifies how the text should be set. Set to zero.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a Unicode string that contains the tooltip text.

### -field iItem

Type: <b>int</b>

Value of type <b>int</b> that contains the 
zero-based index of the item to which this structure refers.

### -field iSubItem

Type: <b>int</b>

Value of type <b>int</b> that contains the one-based index of the subitem to which this structure refers.