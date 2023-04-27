---
UID: NF:shobjidl_core.IMenuPopup.Popup
title: IMenuPopup::Popup (shobjidl_core.h)
description: Invokes the shortcut menu at a specified onscreen location.
helpviewer_keywords: ["IMenuPopup interface [Windows Shell]","Popup method","IMenuPopup.Popup","IMenuPopup::Popup","MPPF_ALIGN_LEFT","MPPF_ALIGN_RIGHT","MPPF_BOTTOM","MPPF_FINALSELECT","MPPF_FORCEZORDER","MPPF_INITIALSELECT","MPPF_KEYBOARD","MPPF_LEFT","MPPF_NOANIMATE","MPPF_POS_MASK","MPPF_REPOSITION","MPPF_RIGHT","MPPF_SETFOCUS","MPPF_TOP","Popup","Popup method [Windows Shell]","Popup method [Windows Shell]","IMenuPopup interface","_win32_IMenuPopup_Popup","shell.IMenuPopup_Popup","shobjidl_core/IMenuPopup::Popup"]
old-location: shell\IMenuPopup_Popup.htm
tech.root: shell
ms.assetid: 2f889955-9c6d-4b6c-ae04-389d2bff3bd9
ms.date: 12/05/2018
ms.keywords: IMenuPopup interface [Windows Shell],Popup method, IMenuPopup.Popup, IMenuPopup::Popup, MPPF_ALIGN_LEFT, MPPF_ALIGN_RIGHT, MPPF_BOTTOM, MPPF_FINALSELECT, MPPF_FORCEZORDER, MPPF_INITIALSELECT, MPPF_KEYBOARD, MPPF_LEFT, MPPF_NOANIMATE, MPPF_POS_MASK, MPPF_REPOSITION, MPPF_RIGHT, MPPF_SETFOCUS, MPPF_TOP, Popup, Popup method [Windows Shell], Popup method [Windows Shell],IMenuPopup interface, _win32_IMenuPopup_Popup, shell.IMenuPopup_Popup, shobjidl_core/IMenuPopup::Popup
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMenuPopup::Popup
 - shobjidl_core/IMenuPopup::Popup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IMenuPopup.Popup
---

# IMenuPopup::Popup


## -description

Invokes the shortcut menu at a specified onscreen location.

## -parameters

### -param ppt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a> structure that specifies the location of the pop-up menu in screen coordinates. The pop-up menu is displayed in relation to this point as determined by the position flags set in <i>dwFlags</i>.

### -param prcExclude [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a> structure that specifies the rectangle to exclude when positioning the menu. In Windows Vista, the alignment of the menu in relation to this area is determined by the alignment flags set in <i>dwFlags</i>. This parameter can be <b>NULL</b> to include the entire screen.

### -param dwFlags [in]

Type: <b>MP_POPUPFLAGS</b>

One or more of the following constants that control the display of the pop-up menu.



#### MPPF_SETFOCUS (0x00000001)

The menu should have focus when it appears.



#### MPPF_INITIALSELECT (0x00000002)

The first item in the menu should be selected.



#### MPPF_NOANIMATE (0x00000004)

Do not animate this show.



#### MPPF_KEYBOARD (0x00000010)

The menu is activated by the keyboard.



#### MPPF_REPOSITION (0x00000020)

Reposition the displayed bar.



#### MPPF_FORCEZORDER (0x00000040)

The menu bar should ignore submenu positions.



#### MPPF_FINALSELECT (0x00000080)

The last item in the menu should be selected.



#### MPPF_TOP (0x20000000)

Display the pop-up menu above the point specified in <i>ppt</i>.



#### MPPF_LEFT (0x40000000)

Display the pop-up menu to the left of the point specified in <i>ppt</i>.



#### MPPF_RIGHT (0x60000000)

Display the pop-up menu to the right of the point specified in <i>ppt</i>.



#### MPPF_BOTTOM (0x80000000)

Display the pop-up menu below the point specified in <i>ppt</i>.



#### MPPF_POS_MASK (0xE0000000)

Mask for position values <b>MPPF_TOP</b>, <b>MPPF_LEFT</b>, and <b>MPPF_RIGHT</b>.



#### MPPF_ALIGN_LEFT (0x02000000)

Default alignment.



#### MPPF_ALIGN_RIGHT (0x04000000)

The pop-up menu should be aligned to the right of the excluded rectangle specified by <i>prcExclude</i>.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the object implements the pop-up menu as a modeless menu. Otherwise, returns <b>S_FALSE</b>, which indicates the end of the implementation for the menu.