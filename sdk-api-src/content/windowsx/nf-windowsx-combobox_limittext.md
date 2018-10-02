---
UID: NF:windowsx.ComboBox_LimitText
title: ComboBox_LimitText macro
author: windows-sdk-content
description: Limits the length of the text the user may type into the edit control of a combo box. You can use this macro or send the CB_LIMITTEXT message explicitly.
old-location: controls\ComboBox_LimitText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\combobox_limittext.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ComboBox_LimitText, ComboBox_LimitText macro [Windows Controls], _win32_ComboBox_LimitText, _win32_ComboBox_LimitText_cpp, controls.ComboBox_LimitText, controls._win32_ComboBox_LimitText, windowsx/ComboBox_LimitText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: windowsx.h
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
 - Windowsx.h
api_name:
 - ComboBox_LimitText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_LimitText macro


## -description


Limits the length of the text the user may type into the edit control of a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/95b7d07a-594b-4096-afbb-4dab77bdc41d">CB_LIMITTEXT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param cchLimit

Type: <b>int</b>

The maximum number of characters.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/95b7d07a-594b-4096-afbb-4dab77bdc41d">CB_LIMITTEXT</a>.



