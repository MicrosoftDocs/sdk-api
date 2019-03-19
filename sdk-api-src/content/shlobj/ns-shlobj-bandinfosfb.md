---
UID: NS:shlobj.__unnamed_struct_1
title: BANDINFOSFB (shlobj.h)
author: windows-sdk-content
description: Contains information about a folder band. This structure is used with the IShellFolderBand::GetBandInfoSFB and IShellFolderBand::SetBandInfoSFB methods.
old-location: shell\BANDINFOSFB.htm
tech.root: shell
ms.assetid: 7067f563-383d-469f-abcf-3e1ea28dc956
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PBANDINFOSFB, BANDINFOSFB, BANDINFOSFB structure [Windows Shell], ISFBVIEWMODE_LARGEICONS, ISFBVIEWMODE_LOGOS, ISFBVIEWMODE_SMALLICONS, ISFB_MASK_BKCOLOR, ISFB_MASK_COLORS, ISFB_MASK_IDLIST, ISFB_MASK_SHELLFOLDER, ISFB_MASK_STATE, ISFB_MASK_VIEWMODE, ISFB_STATE_ALLOWRENAME, ISFB_STATE_BTNMINSIZE, ISFB_STATE_CHANNELBAR, ISFB_STATE_DEBOSSED, ISFB_STATE_DEFAULT, ISFB_STATE_FULLOPEN, ISFB_STATE_NONAMESORT, ISFB_STATE_NOSHOWTEXT, ISFB_STATE_QLINKSMODE, PBANDINFOSFB, PBANDINFOSFB structure pointer [Windows Shell], _win32_BANDINFOSFB, shell.BANDINFOSFB, shlobj/BANDINFOSFB, shlobj/PBANDINFOSFB"
ms.topic: struct
req.header: shlobj.h
req.include-header: 
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
 - Shlobj.h
api_name:
 - BANDINFOSFB
product: Windows
targetos: Windows
req.typenames: BANDINFOSFB, *PBANDINFOSFB
req.redist: 
---

# BANDINFOSFB structure


## -description


Contains information about a folder band. This structure is used with the <a href="https://msdn.microsoft.com/7a42ba12-987a-4b43-9d95-085a5e896245">IShellFolderBand::GetBandInfoSFB</a> and <a href="https://msdn.microsoft.com/6b1a219f-60a3-4073-8293-2e9e1c6459d9">IShellFolderBand::SetBandInfoSFB</a> methods.


## -struct-fields




### -field dwMask

Type: <b>DWORD</b>

A mask that indicates which members of this <b>BANDINFOSFB</b> structure are valid.  One or more of the following values.



#### ISFB_MASK_STATE (0x00000001)

The <b>dwStateMask</b> member is valid.



#### ISFB_MASK_BKCOLOR (0x00000002)

The <b>crBkgnd</b> member is valid.



#### ISFB_MASK_VIEWMODE (0x00000004)

The <b>wViewMode</b> member is valid.



#### ISFB_MASK_SHELLFOLDER (0x00000008)

The <b>psf</b> member is valid.



#### ISFB_MASK_IDLIST (0x00000010)

The <b>pidl</b> member is valid.



#### ISFB_MASK_COLORS (0x00000020)

The <b>crBtnLt</b> and <b>crBtnDk</b> members are valid.


### -field dwStateMask

Type: <b>DWORD</b>

A mask that indicates which of the <b>dwState</b> bits are valid to be set or queried. One or more of the following values.



#### ISFB_STATE_DEFAULT (0x00000000)

None of the <b>dwState</b> bits.



#### ISFB_STATE_DEBOSSED (0x00000001)

Displays the object with a debossed state, which is with a sunken appearance.



#### ISFB_STATE_ALLOWRENAME (0x00000002)

Allow renaming and a context menu.



#### ISFB_STATE_NOSHOWTEXT (0x00000004)

Do not show text.



#### ISFB_STATE_CHANNELBAR (0x00000010)

Deprecated.



#### ISFB_STATE_QLINKSMODE (0x00000020)

Deprecated.



#### ISFB_STATE_FULLOPEN (0x00000040)

Maximize when opened.



#### ISFB_STATE_NONAMESORT (0x00000080)

The band does not sort by name.



#### ISFB_STATE_BTNMINSIZE (0x00000100)

The band reports the minimum size of its button when queried.


### -field dwState

Type: <b>DWORD</b>

State bits. One of the values listed for <b>dwStateMask</b>.


### -field crBkgnd

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> that contains the background color of the band.


### -field crBtnLt

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>


<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> that contains the light button color.


### -field crBtnDk

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>


<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> that contains the dark button color.


### -field wViewMode

Type: <b>WORD</b>

View mode of the band. One of the following values.



#### ISFBVIEWMODE_SMALLICONS (0x00000001)

Use small icons on the folder band.



#### ISFBVIEWMODE_LARGEICONS (0x00000002)

Use large icons on the folder band.



#### ISFBVIEWMODE_LOGOS (0x00000003a)

<b>Not supported under Windows Vista or later. Not supported under Internet Explorer version 7 or later.</b>


### -field wAlign

Type: <b>WORD</b>


### -field psf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> object.


### -field pidl

Type: <b>PIDLIST_ABSOLUTE</b>

A PIDL.
        

