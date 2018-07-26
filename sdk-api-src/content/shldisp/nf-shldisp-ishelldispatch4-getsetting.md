---
UID: NF:shldisp.IShellDispatch4.GetSetting
title: IShellDispatch4::GetSetting
author: windows-sdk-content
description: Retrieves a global Shell setting.
old-location: shell\IShellDispatch4_GetSetting.htm
old-project: shell
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: GetSetting, GetSetting method [Windows Shell], GetSetting method [Windows Shell],IShellDispatch4 object, IShellDispatch4 object [Windows Shell],GetSetting method, IShellDispatch4.GetSetting, IShellDispatch4::GetSetting, SSF_AUTOCHECKSELECT, SSF_DESKTOPHTML, SSF_DONTPRETTYPATH, SSF_DOUBLECLICKINWEBVIEW, SSF_FILTER, SSF_HIDDENFILEEXTS, SSF_HIDEICONS, SSF_ICONSONLY, SSF_MAPNETDRVBUTTON, SSF_NOCONFIRMRECYCLE, SSF_NONETCRAWLING, SSF_SEPPROCESS, SSF_SERVERADMINUI, SSF_SHOWALLOBJECTS, SSF_SHOWATTRIBCOL, SSF_SHOWCOMPCOLOR, SSF_SHOWEXTENSIONS, SSF_SHOWINFOTIP, SSF_SHOWSTARTPAGE, SSF_SHOWSUPERHIDDEN, SSF_SHOWSYSFILES, SSF_SHOWTYPEOVERLAY, SSF_SORTCOLUMNS, SSF_STARTPANELON, SSF_WEBVIEW, SSF_WIN95CLASSIC, _shell_IShellDispatch4_GetSetting, shell.IShellDispatch4_GetSetting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDispatch4.GetSetting
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch4::GetSetting


## -description


Retrieves a global Shell setting.


## -parameters




### -param lSetting [in]

Type: <b>long</b>

A value that specifies the current Shell setting to retrieve. Only one setting can be retrieved in each call. The following values are recognized by this method.



#### SSF_AUTOCHECKSELECT (0x00800000)

<b>Windows Vista and later</b>. The state of the <b>Use check boxes to select items</b> option. This option is enabled automatically when the system has a pen input device configured.



#### SSF_DESKTOPHTML (0x00000200)

Not used.



#### SSF_DONTPRETTYPATH (0x00000800)

The state of the <b>Allow all uppercase names</b> option. As of Windows Vista, this folder option is no longer available.



#### SSF_DOUBLECLICKINWEBVIEW (0x00000080)

The state of the <b>Double-click to open an item (single-click to select)</b> option.



#### SSF_FILTER (0x00010000)

Not used.



#### SSF_HIDDENFILEEXTS (0x00000004)

Not used.



#### SSF_HIDEICONS (0x00004000)

The state of icon display in the Windows Explorer list view. If this option is active, no icons are displayed in the list view.



#### SSF_ICONSONLY (0x01000000)

<b>Windows Vista and later</b>. The state of display name display in the Windows Explorer list view. If this option is active, icons are displayed in the list view, but display names are not.



#### SSF_MAPNETDRVBUTTON (0x00001000)

The state of the <b>Show map network drive button in toolbar</b> option. As of Windows Vista, this option is no longer available.



#### SSF_NOCONFIRMRECYCLE (0x00008000)

The state of the Recycle Bin's <b>Display delete confirmation dialog</b> option.



#### SSF_NONETCRAWLING (0x00100000)

The state of the <b>Automatically search for network folders and printers</b> option. As of Windows Vista, this option is no longer available.



#### SSF_SEPPROCESS (0x00080000)

The state of the <b>Launch folder windows in a separate process</b> option.



#### SSF_SERVERADMINUI (0x00000004)

Not used.



#### SSF_SHOWALLOBJECTS (0x00000001)

The state of the <b>Hidden files and folders</b> option.



#### SSF_SHOWATTRIBCOL (0x00000100)

The state of the <b>Show File Attributes in Detail View</b> option. As of Windows Vista, this option is no longer available.



#### SSF_SHOWCOMPCOLOR (0x00000008)

The state of the <b>Show encrypted or compressed NTFS files in color</b> option.



#### SSF_SHOWEXTENSIONS (0x00000002)

The state of the <b>Hide extensions for known file types</b> option.



#### SSF_SHOWINFOTIP (0x00002000)

The state of the <b>Show pop-up description for folder and desktop items</b> option.



#### SSF_SHOWSTARTPAGE (0x00400000)

Not used.



#### SSF_SHOWSUPERHIDDEN (0x00040000)

The state of the <b>Hide protected operating system files</b> option.



#### SSF_SHOWSYSFILES (0x00000020)

The state of the <b>Hidden files and folders</b> option. In Windows Vista and later, this is equivalent to SSF_SHOWALLOBJECTS. In versions of Windows before Windows Vista, this value referred to the state of the <b>Do not show hidden files and folders</b> option.



#### SSF_SHOWTYPEOVERLAY (0x02000000)

<b>Windows Vista and later</b>. The state of the <b>Display file icon on thumbnails</b> option. If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.



#### SSF_SORTCOLUMNS (0x00000010)

Not used.



#### SSF_STARTPANELON (0x00200000)

The state of the Windows XP display option, which selects between the Windows XP style and the classic style. As of Windows Vista, this option is no longer available.



#### SSF_WEBVIEW (0x00020000)

The state of the <b>Display as a web view option</b>. As of Windows Vista, this option is no longer available.



#### SSF_WIN95CLASSIC (0x00000400)

The state of the <b>Classic Style</b> option. As of Windows Vista, this option is no longer available.


### -param pResult






## -returns



<h3>JScript</h3>
Type: <b>VARIANT_BOOL*</b>

Set to <b>true</b> if the setting exists; otherwise, <b>false</b>.

<h3>VB</h3>
Type: <b>VARIANT_BOOL*</b>

Set to <b>true</b> if the setting exists; otherwise, <b>false</b>.



