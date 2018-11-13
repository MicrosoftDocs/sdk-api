---
UID: NS:winuser.tagTPMPARAMS
title: tagTPMPARAMS
author: windows-sdk-content
description: Contains extended parameters for the TrackPopupMenuEx function.
old-location: menurc\tpmparams.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\tpmparams.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - TPMPARAMS
product: Windows
targetos: Windows
req.typenames: TPMPARAMS
req.redist: 
---

# tagTPMPARAMS structure


## -description


Contains extended parameters for the <a href="https://msdn.microsoft.com/en-us/library/ms648003(v=VS.85).aspx">TrackPopupMenuEx</a> function.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of structure, in bytes. 


### -field rcExclude

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The rectangle to be excluded when positioning the window, in screen coordinates. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648003(v=VS.85).aspx">TrackPopupMenuEx</a>
 

 

