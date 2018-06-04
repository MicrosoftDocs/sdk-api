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

# IMenuPopup::Popup


## -description


Invokes the shortcut menu at a specified onscreen location.


## -parameters




### -param ppt [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that specifies the location of the pop-up menu in screen coordinates. The pop-up menu is displayed in relation to this point as determined by the position flags set in <i>dwFlags</i>.


### -param prcExclude [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that specifies the rectangle to exclude when positioning the menu. In Windows Vista, the alignment of the menu in relation to this area is determined by the alignment flags set in <i>dwFlags</i>. This parameter can be <b>NULL</b> to include the entire screen.


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



