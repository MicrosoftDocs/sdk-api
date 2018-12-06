---
UID: NF:winuser.MAKELPARAM
title: MAKELPARAM macro
author: windows-sdk-content
description: Creates a value for use as an lParam parameter in a message. The macro concatenates the specified values.
old-location: winmsg\makelparam.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmacros\makelparam.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MAKELPARAM, MAKELPARAM macro [Windows and Messages], _win32_MAKELPARAM, _win32_makelparam_cpp, winmsg.makelparam, winui._win32_makelparam, winuser/MAKELPARAM
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
 - MAKELPARAM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MAKELPARAM macro


## -description


Creates a value for use as an
			<i>lParam</i> parameter in a message. The macro concatenates the specified values. 


## -parameters




### -param l

The low-order word of the new value. 


### -param h

The high-order word of the new value. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/161979a1-296c-47ed-bf41-74a561b5ba05">MAKELONG</a>



<a href="https://msdn.microsoft.com/8a86594d-05cd-44e4-aceb-3541e4d3af16">MAKELRESULT</a>



<a href="https://msdn.microsoft.com/029f334b-53f6-46cf-8fa7-613bf241d0e6">MAKEWPARAM</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>
 

 

