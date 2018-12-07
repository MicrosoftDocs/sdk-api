---
UID: NF:winuser.MAKEWPARAM
title: MAKEWPARAM macro
author: windows-sdk-content
description: Creates a value for use as a wParam parameter in a message. The macro concatenates the specified values.
old-location: winmsg\makewparam.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmacros\makewparam.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MAKEWPARAM, MAKEWPARAM macro [Windows and Messages], _win32_MAKEWPARAM, _win32_makewparam_cpp, winmsg.makewparam, winui._win32_makewparam, winuser/MAKEWPARAM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - MAKEWPARAM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MAKEWPARAM macro


## -description


Creates a value for use as a <i>wParam</i> parameter in a message. The macro concatenates the specified values.


## -parameters




### -param l

The low-order word of the new value.


### -param h

The high-order word of the new value.


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632660(v=VS.85).aspx">MAKELONG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632661(v=VS.85).aspx">MAKELPARAM</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632662(v=VS.85).aspx">MAKELRESULT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>
 

 

