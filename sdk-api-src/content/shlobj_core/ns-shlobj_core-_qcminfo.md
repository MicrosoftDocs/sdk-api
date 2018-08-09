---
UID: NS:shlobj_core._QCMINFO
title: "_QCMINFO"
author: windows-sdk-content
description: Contains information for merging menu items into Windows Explorer menus.
old-location: shell\QCMINFO_str.htm
old-project: shell
ms.assetid: 3f991ebb-d66c-4bdc-b9d2-2bf6bb5a269a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPQCMINFO, QCMINFO, QCMINFO structure [Windows Shell], _QCMINFO, _win32_QCMINFO_str, shell.QCMINFO_str, shlobj_core/QCMINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: QCMINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - QCMINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _QCMINFO structure


## -description


Contains information for merging menu items into Windows Explorer menus.


## -struct-fields




### -field hmenu

Type: <b>HMENU</b>

[in] The handle of the menu where the new commands are to be added.


### -field indexMenu

Type: <b>UINT</b>

[in] The zero-based index where the first menu item are to be inserted.


### -field idCmdFirst

Type: <b>UINT</b>

[in, out] On entry, this member contains the first available ID to be used for the context menu. On exit, it contains the last ID added plus one.


### -field idCmdLast

Type: <b>UINT</b>

[in] The maximum value for a menu item identifier. The difference between the input value of <b>idCmdFirst</b> and <b>idCmdLast</b> is the maximum number of menu items that can be added.


### -field pIdMap

Type: <b>QCMINFO_IDMAP*</b>

Not used, must be <b>NULL</b>.


## -remarks



See <a href="https://msdn.microsoft.com/329fe15b-c1c1-4ffd-812e-9e74451bad6e">IContextMenu::QueryContextMenu</a> as this structure performs the same role as the parameters of that method. Note, however, that the information provided by the return value of that method is not a parallel to the information provided by the return value of an operation involving <b>QCMINFO</b>.




## -see-also




<a href="https://msdn.microsoft.com/2fd779ac-7dd6-4b81-86dc-8930db27ae59">DFM_MERGECONTEXTMENU</a>



<a href="https://msdn.microsoft.com/37414335-4f3c-461e-bd05-d6ef850f972a">DFM_MERGECONTEXTMENU_BOTTOM</a>



<a href="https://msdn.microsoft.com/eed6aec6-11a0-4738-b5b9-a455d0e35eac">DFM_MERGECONTEXTMENU_TOP</a>



<a href="https://msdn.microsoft.com/59bb99a3-9a5a-4ea5-9830-b04d7d886b3f">SFVM_MERGEMENU</a>
 

 

