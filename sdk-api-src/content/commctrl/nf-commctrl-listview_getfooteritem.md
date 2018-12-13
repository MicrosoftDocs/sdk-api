---
UID: NF:commctrl.ListView_GetFooterItem
title: ListView_GetFooterItem macro
author: windows-sdk-content
description: Gets information on a footer item for a specified list-view control. Use this macro or send the LVM_GETFOOTERITEM message explicitly.
old-location: controls\ListView_GetFooterItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfooteritem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_GetFooterItem, ListView_GetFooterItem macro [Windows Controls], _shell_ListView_GetFooterItem, _shell_ListView_GetFooterItem_cpp, commctrl/ListView_GetFooterItem, controls.ListView_GetFooterItem, controls._shell_ListView_GetFooterItem
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
 - ListView_GetFooterItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetFooterItem macro


## -description


Gets information on a footer item for a specified list-view control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774928(v=VS.85).aspx">LVM_GETFOOTERITEM</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param iItem [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An index of the item.


### -param pfi [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774750(v=VS.85).aspx">LVFOOTERITEM</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb774750(v=VS.85).aspx">LVFOOTERITEM</a> structure to receive a value for the <i>state</i> and/or <i>pszText</i> members according to the value of the <i>mask</i> member. The caller is responsible for allocating this structure and setting its members to indicate to the receiver what information to return. For more information, see <b>LVFOOTERITEM</b>.

