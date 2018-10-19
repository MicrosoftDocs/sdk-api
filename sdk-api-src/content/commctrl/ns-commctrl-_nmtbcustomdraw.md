---
UID: NS:commctrl._NMTBCUSTOMDRAW
title: "_NMTBCUSTOMDRAW"
author: windows-sdk-content
description: Contains information specific to an NM_CUSTOMDRAW notification code sent by a toolbar control.
old-location: controls\NMTBCUSTOMDRAW.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbcustomdraw.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*LPNMTBCUSTOMDRAW, LPNMTBCUSTOMDRAW, LPNMTBCUSTOMDRAW structure pointer [Windows Controls], NMTBCUSTOMDRAW, NMTBCUSTOMDRAW structure [Windows Controls], _NMTBCUSTOMDRAW, _win32_NMTBCUSTOMDRAW, _win32_NMTBCUSTOMDRAW_cpp, commctrl/LPNMTBCUSTOMDRAW, commctrl/NMTBCUSTOMDRAW, controls.NMTBCUSTOMDRAW, controls._win32_NMTBCUSTOMDRAW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
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
 - Commctrl.h
api_name:
 - NMTBCUSTOMDRAW
product: Windows
targetos: Windows
req.typenames: NMTBCUSTOMDRAW, *LPNMTBCUSTOMDRAW
req.redist: 
---

# _NMTBCUSTOMDRAW structure


## -description


Contains information specific to an <a href="https://msdn.microsoft.com/en-us/library/Bb760492(v=VS.85).aspx">NM_CUSTOMDRAW</a> notification code sent by a toolbar control. 


## -struct-fields




### -field nmcd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775483(v=VS.85).aspx">NMCUSTOMDRAW</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775483(v=VS.85).aspx">NMCUSTOMDRAW</a> structure that contains general custom draw information. The 
					<b>uItemState</b> member of this structure can be modified so that a toolbar item will be drawn in the specified state without actually changing the item's state. 


### -field hbrMonoDither

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBRUSH</a></b>

HBRUSH that the control will use when drawing the background of marked or dithered items. This member is ignored if TBCDRF_NOMARK is returned from the <a href="https://msdn.microsoft.com/en-us/library/Bb760492(v=VS.85).aspx">NM_CUSTOMDRAW</a> notification code. 


### -field hbrLines

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBRUSH</a></b>

HBRUSH that the control will use when drawing lines on the buttons. 


### -field hpenLines

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HPEN</a></b>

HPEN that the control will use when drawing lines on the buttons. 


### -field clrText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>


<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> that represents the color that the control will use when drawing text on normal items. 


### -field clrMark

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> that represents the background color that the control will use when drawing text on marked items. 


### -field clrTextHighlight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> that represents the color that the control will use when drawing text on highlighted items. 


### -field clrBtnFace

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> that represents the face color that the control will use when drawing buttons. 


### -field clrBtnHighlight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> that represents the face color that the control will use when drawing highlighted items. An item is highlighted if it has the <a href="https://msdn.microsoft.com/en-us/library/Bb760437(v=VS.85).aspx">TBSTATE_MARKED</a> style and is contained in a toolbar that has the <a href="https://msdn.microsoft.com/en-us/library/Bb760439(v=VS.85).aspx">TBSTYLE_FLAT</a> style. 


### -field clrHighlightHotTrack

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> that represents the background color that the control will use when drawing text on hot tracked items. This member is ignored if TBCDRF_HILITEHOTTRACK is not returned from the <a href="https://msdn.microsoft.com/en-us/library/Bb760492(v=VS.85).aspx">NM_CUSTOMDRAW</a> notification code. 


### -field rcText

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that, on entry, contains the rectangle of the item's text. The 
					<b>right</b> and 
					<b>bottom</b> members of this structure can be modified to change the width and height, respectively, of the text rectangle of the item. 


### -field nStringBkMode

Type: <b>int</b>

Background mode that the control will use when drawing the text of a nonhighlighted item. This can be either the TRANSPARENT or OPAQUE value. 


### -field nHLStringBkMode

Type: <b>int</b>

Background mode that the control will use when drawing the text of a highlighted item. This can be either the TRANSPARENT or OPAQUE value. 


### -field iListGap

Type: <b>int</b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0</a> Specifies the distance between the toolbar button image and the text, in logical pixels, for toolbars that have <a href="https://msdn.microsoft.com/en-us/library/Bb760439(v=VS.85).aspx">TBSTYLE_LIST</a> style set.

Note that Comctl32.dll version 6 is not redistributable but it is included in Windows or later. To use Comctl32.dll version 6, specify it in a manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.

