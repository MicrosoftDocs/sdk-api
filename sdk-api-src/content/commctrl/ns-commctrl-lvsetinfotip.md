---
UID: NS:commctrl.tagLVSETINFOTIP
title: LVSETINFOTIP
author: windows-sdk-content
description: Provides information about tooltip text that is to be set.
old-location: controls\LVSETINFOTIP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvsetinfotip.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PLVSETINFOTIP, LVSETINFOTIP, LVSETINFOTIP structure [Windows Controls], PLVSETINFOTIP, PLVSETINFOTIP structure pointer [Windows Controls], commctrl/LVSETINFOTIP, commctrl/PLVSETINFOTIP, controls.LVSETINFOTIP, controls.inet_LVSETINFOTIP, inet_LVSETINFOTIP, inet_LVSETINFOTIP_cpp"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - LVSETINFOTIP
product: Windows
targetos: Windows
req.typenames: LVSETINFOTIP, *PLVSETINFOTIP
req.redist: 
---

# LVSETINFOTIP structure


## -description


Provides information about tooltip text that is to be set.  



## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the <b>LVSETINFOTIP</b> structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Flag that specifies how the text should be set. Set to zero.


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

Pointer to a Unicode string that contains the tooltip text.


### -field iItem

Type: <b>int</b>

Value of type <b>int</b> that contains the 
zero-based index of the item to which this structure refers. 


### -field iSubItem

Type: <b>int</b>

Value of type <b>int</b> that contains the one-based index of the subitem to which this structure refers.

