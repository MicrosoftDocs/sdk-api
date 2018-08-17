---
UID: NS:richedit._formatrange
title: "_formatrange"
author: windows-sdk-content
description: Information that a rich edit control uses to format its output for a particular device. This structure is used with the EM_FORMATRANGE message.
old-location: controls\FORMATRANGE.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\formatrange.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FORMATRANGE, FORMATRANGE structure [Windows Controls], _formatrange, _win32_FORMATRANGE_str, _win32_FORMATRANGE_str_cpp, controls.FORMATRANGE, controls._win32_FORMATRANGE_str, richedit/FORMATRANGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FORMATRANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - FORMATRANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _formatrange structure


## -description


Information that a rich edit control uses to format its output for a particular device. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb788020(v=VS.85).aspx">EM_FORMATRANGE</a> message.


## -struct-fields




### -field hdcTarget

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

An HDC for the target device to format for. 


### -field hdc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

A HDC for the device to render to, if <a href="https://msdn.microsoft.com/en-us/library/Bb788020(v=VS.85).aspx">EM_FORMATRANGE</a> is being used to send the output to a device.


### -field rc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The area within the <i>rcPage</i> rectangle to render to. Units are measured in twips. 


### -field rcPage

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

The entire area of a page on the rendering device. Units are measured in twips. 


### -field chrg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a></b>

The range of characters to format.


## -remarks



<b>hdcTarget</b> contains the HDC to format for, which is usually the same as the HDC specified by <b>hdc</b> but can be different. For example, if you create a print preview module, <b>hdc</b> is the HDC of the window in which the output is viewed, and <b>hdcTarget</b> is the HDC for the printer. 
	

The values for <b>rc</b> and <b>rcPage</b> can be obtained by using <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb788020(v=VS.85).aspx">EM_FORMATRANGE</a>
 

 

