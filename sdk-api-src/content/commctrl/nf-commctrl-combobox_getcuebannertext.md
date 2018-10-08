---
UID: NF:commctrl.ComboBox_GetCueBannerText
title: ComboBox_GetCueBannerText macro
author: windows-sdk-content
description: Gets the cue banner text displayed in the edit control of a combo box. Use this macro or send the CB_GETCUEBANNER message explicitly.
old-location: controls\ComboBox_GetCueBannerText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getcuebannertext.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
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
---

# ComboBox_GetCueBannerText macro


## -description


Gets the cue banner text displayed in the edit control of a combo box. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775843(v=VS.85).aspx">CB_GETCUEBANNER</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the combo box.


### -param lpwText

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPWSTR</a></b>

A pointer to a Unicode string buffer that receives the cue banner text. The calling application is responsible for allocating the memory for the buffer. The buffer size must be equal to the length of the cue banner string in <b>WCHAR</b><b>s</b>, plus 1—for the terminating <b>NULL</b> <b>WCHAR</b>.


### -param cchText

Type: <b>int</b>

The size of the buffer pointed to by <i>lpwText</i> in <b>WCHAR</b><b>s</b>. 
               


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775793(v=VS.85).aspx">Combo Box Features</a>
 

 

