---
UID: NF:shlwapi.SHAutoComplete
title: SHAutoComplete function (shlwapi.h)
description: Instructs system edit controls to use AutoComplete to help complete URLs or file system paths.
helpviewer_keywords: ["SHACF_AUTOAPPEND_FORCE_OFF","SHACF_AUTOAPPEND_FORCE_ON","SHACF_AUTOSUGGEST_FORCE_OFF","SHACF_AUTOSUGGEST_FORCE_ON","SHACF_DEFAULT","SHACF_FILESYSTEM","SHACF_FILESYS_DIRS","SHACF_FILESYS_ONLY","SHACF_URLALL","SHACF_URLHISTORY","SHACF_URLMRU","SHACF_USETAB","SHACF_VIRTUAL_NAMESPACE","SHAutoComplete","SHAutoComplete function [Windows Shell]","_win32_ShAutoComplete","shell.SHAutoComplete","shlwapi/SHAutoComplete"]
old-location: shell\SHAutoComplete.htm
tech.root: shell
ms.assetid: b47efa8d-2118-4805-bb04-97bd143228dc
ms.date: 12/05/2018
ms.keywords: SHACF_AUTOAPPEND_FORCE_OFF, SHACF_AUTOAPPEND_FORCE_ON, SHACF_AUTOSUGGEST_FORCE_OFF, SHACF_AUTOSUGGEST_FORCE_ON, SHACF_DEFAULT, SHACF_FILESYSTEM, SHACF_FILESYS_DIRS, SHACF_FILESYS_ONLY, SHACF_URLALL, SHACF_URLHISTORY, SHACF_URLMRU, SHACF_USETAB, SHACF_VIRTUAL_NAMESPACE, SHAutoComplete, SHAutoComplete function [Windows Shell], _win32_ShAutoComplete, shell.SHAutoComplete, shlwapi/SHAutoComplete
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAutoComplete
 - shlwapi/SHAutoComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
api_name:
 - SHAutoComplete
---

# SHAutoComplete function


## -description

Instructs system edit controls to use AutoComplete to help complete URLs or file system paths.

## -parameters

### -param hwndEdit [in]

Type: <b>HWND</b>

The window handle of a system edit control. Typically, this parameter is the handle of an edit control or the edit control embedded in a <a href="/windows/desktop/Controls/comboboxex-control-reference">ComboBoxEx</a> control.

### -param dwFlags

Type: <b>DWORD</b>

The flags to control the operation of <b>SHAutoComplete</b>. The first four flags are used to override the Internet Explorer registry settings. The user can change these settings manually by launching the <b>Internet Options</b> property sheet from the <b>Tools</b> menu and clicking the <b>Advanced</b> tab.



#### SHACF_AUTOAPPEND_FORCE_OFF (0x80000000)

Ignore the registry default and force the AutoAppend feature off. This flag must be used in combination with one or more of the SHACF_FILESYS* or SHACF_URL* flags.



#### SHACF_AUTOAPPEND_FORCE_ON (0x40000000)

Ignore the registry value and force the AutoAppend feature on. The completed string will be displayed in the edit box with the added characters highlighted. This flag must be used in combination with one or more of the SHACF_FILESYS* or SHACF_URL* flags.



#### SHACF_AUTOSUGGEST_FORCE_OFF (0x20000000)

Ignore the registry default and force the AutoSuggest feature off. This flag must be used in combination with one or more of the SHACF_FILESYS* or SHACF_URL* flags.



#### SHACF_AUTOSUGGEST_FORCE_ON (0x10000000)

Ignore the registry value and force the AutoSuggest feature on. A selection of possible completed strings will be displayed as a drop-down list, below the edit box. This flag must be used in combination with one or more of the SHACF_FILESYS* or SHACF_URL* flags.



#### SHACF_DEFAULT (0x00000000)

The default setting, equivalent to <b>SHACF_FILESYSTEM</b> | <b>SHACF_URLALL</b>. <b>SHACF_DEFAULT</b> cannot be combined with any other flags.



#### SHACF_FILESYS_ONLY (0x00000010)

Include the file system only.



#### SHACF_FILESYS_DIRS (0x00000020)

Include the file system and directories, UNC servers, and UNC server shares.



#### SHACF_FILESYSTEM (0x00000001)

Include the file system and the rest of the Shell (Desktop, Computer, and Control Panel, for example).



#### SHACF_URLALL (SHACF_URLHISTORY | SHACF_URLMRU)

Include the URLs in the users <b>History</b> and <b>Recently Used</b> lists. Equivalent to <b>SHACF_URLHISTORY</b> | <b>SHACF_URLMRU</b>.



#### SHACF_URLHISTORY (0x00000002)

Include the URLs in the user's <b>History</b> list.



#### SHACF_URLMRU (0x00000004)

Include the URLs in the user's <b>Recently Used</b> list.



#### SHACF_USETAB (0x00000008)

Allow the user to select from the autosuggest list by pressing the TAB key. If this flag is not set, pressing the TAB key will shift focus to the next control and close the autosuggest list. If <b>SHACF_USETAB</b> is set, pressing the TAB key will select the first item in the list. Pressing TAB again will select the next item in the list, and so on. When the user reaches the end of the list, the next TAB key press will cycle the focus back to the edit control. This flag must be used in combination with one or more of the SHACF_FILESYS* or SHACF_URL* flags listed on this page.



#### SHACF_VIRTUAL_NAMESPACE (0x00000040)

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SHAutoComplete</b> works on any system edit control, including the edit control and controls that contain edit controls such as <a href="/windows/desktop/Controls/comboboxex-control-reference">ComboBoxEx</a> controls. To retrieve a handle to an edit control embedded in a ComboBoxEx control, send the ComboBoxEx control a <a href="/windows/desktop/Controls/cbem-geteditcontrol">CBEM_GETEDITCONTROL</a> message.

An application must have invoked either <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> prior to calling this function. <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a> cannot be called until the edit box has finished processing the <a href="/windows/desktop/winmsg/wm-destroy">WM_DESTROY</a> message for <i>hwndEdit</i>.

The maximum number of items that can be displayed in an autosuggest drop-down list box is 1000.

On versions of Windows prior to Windows Vista and server versions prior to Windows Server 2008, <b>SHAutoComplete</b> should not be called more than once with the same <b>HWND</b>. Doing so results in a memory leak. It prevents the original resources from being released, including the previous instance of the AutoComplete object, enumerator objects that the previous AutoComplete object has referenced, and Windows Graphics Device Interface (GDI) resources. Rather than call <b>SHAutoComplete</b> again with a different set of flags to change the AutoComplete list, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_AutoComplete to obtain the AutoComplete object. Then pass the <b>HWND</b> to the object to initialize it and provide your own custom enumerator. You can use CLSID_ACLMulti if you want AutoComplete to use multiple lists.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/bb776884(v=vs.85)">Using Autocomplete</a>