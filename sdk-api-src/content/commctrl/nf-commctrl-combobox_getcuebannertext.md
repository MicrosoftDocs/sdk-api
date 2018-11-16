---
UID: NF:commctrl.ComboBox_GetCueBannerText
title: ComboBox_GetCueBannerText macro
author: windows-sdk-content
description: Gets the cue banner text displayed in the edit control of a combo box. Use this macro or send the CB_GETCUEBANNER message explicitly.
old-location: controls\ComboBox_GetCueBannerText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getcuebannertext.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ComboBox_GetCueBannerText, ComboBox_GetCueBannerText macro [Windows Controls], _shell_ComboBox_GetCueBannerText, _shell_ComboBox_GetCueBannerText_cpp, commctrl/ComboBox_GetCueBannerText, controls.ComboBox_GetCueBannerText, controls._shell_ComboBox_GetCueBannerText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ComboBox_GetCueBannerText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ComboBox_GetCueBannerText
: 
---

# ComboBox_GetCueBannerText macro


## -description


Gets the cue banner text displayed in the edit control of a combo box. Use this macro or send the <a href="https://msdn.microsoft.com/38959228-9f07-4636-a1ea-681efe77b9ec">CB_GETCUEBANNER</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the combo box.


### -param lpwText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

A pointer to a Unicode string buffer that receives the cue banner text. The calling application is responsible for allocating the memory for the buffer. The buffer size must be equal to the length of the cue banner string in <b>WCHAR</b><b>s</b>, plus 1—for the terminating <b>NULL</b> <b>WCHAR</b>.


### -param cchText

Type: <b>int</b>

The size of the buffer pointed to by <i>lpwText</i> in <b>WCHAR</b><b>s</b>. 
               


## -see-also




<a href="https://msdn.microsoft.com/7102beff-7f67-4e4e-a32b-9ccae1522ebd">Combo Box Features</a>
 

 

