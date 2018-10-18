---
UID: NF:shldisp.IAutoComplete.Init
title: IAutoComplete::Init
author: windows-sdk-content
description: Initializes the autocomplete object.
old-location: shell\IAutoComplete_Init.htm
tech.root: shell
ms.assetid: e5ee36b7-11b4-4eca-ae8e-eefa6245f287
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IAutoComplete interface [Windows Shell],Init method, IAutoComplete.Init, IAutoComplete::Init, Init, Init method [Windows Shell], Init method [Windows Shell],IAutoComplete interface, _win32_IAutoComplete_Init, shell.IAutoComplete_Init, shldisp/IAutoComplete::Init
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IAutoComplete.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutoComplete::Init


## -description


Initializes the autocomplete object.


## -parameters




### -param hwndEdit [in]

Type: <b>HWND</b>

A handle to the window for the system edit control for which autocompletion will be enabled.


### -param punkACL [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the string list object that generates candidates for the completed string. The object must expose an <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> interface.


### -param pwszRegKeyPath [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional, null-terminated Unicode string that gives the registry path, including the value name, where the format string is stored as a <b>REG_SZ</b> value. The autocomplete object first looks for the path under <b>HKEY_CURRENT_USER</b>. If it fails, it tries <b>HKEY_LOCAL_MACHINE</b>. For a discussion of the format string, see the definition of <i>pwszQuickComplete</i>.


### -param pwszQuickComplete [in, optional]

Type: <b>LPCWSTR</b>

A pointer to an optional null-terminated Unicode string that specifies the format to be used if the user enters text and presses CTRL+ENTER. Set this parameter to <b>NULL</b> to disable quick completion. Otherwise, the autocomplete object treats <i>pwszQuickComplete</i> as a <a href="https://msdn.microsoft.com/en-us/library/ms647541(v=VS.85).aspx">StringCchPrintf</a> format string and the text in the edit box as its associated argument, to produce a new string. For example, set <i>pwszQuickComplete</i> to "http://www.%s.com/". When a user enters "MyURL" into the edit box and presses CTRL+ENTER, the text in the edit box is updated to "http://www.MyURL.com/".


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bed6eb41-3086-4af7-8c75-651da9dba3b2">IAutoComplete</a>
 

 

