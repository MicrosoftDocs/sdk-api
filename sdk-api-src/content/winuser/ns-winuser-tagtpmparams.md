---
UID: NS:winuser.tagTPMPARAMS
title: tagTPMPARAMS
author: windows-sdk-content
description: Contains extended parameters for the TrackPopupMenuEx function.
old-location: menurc\tpmparams.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\tpmparams.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPTPMPARAMS, LPTPMPARAMS, LPTPMPARAMS structure pointer [Menus and Other Resources], TPMPARAMS, TPMPARAMS structure [Menus and Other Resources], _win32_TPMPARAMS_str, _win32_tpmparams_str_cpp, menurc.tpmparams, tagTPMPARAMS, winui._win32_tpmparams_str, winuser/LPTPMPARAMS, winuser/TPMPARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: TPMPARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winuser.h
api_name:
-	TPMPARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagTPMPARAMS structure


## -description


Contains extended parameters for the <a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a> function.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of structure, in bytes. 


### -field rcExclude

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The rectangle to be excluded when positioning the window, in screen coordinates. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/86b8f21b-0dfe-462e-a34a-c80ee5c1d185">TrackPopupMenuEx</a>
 

 

