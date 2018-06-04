---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



