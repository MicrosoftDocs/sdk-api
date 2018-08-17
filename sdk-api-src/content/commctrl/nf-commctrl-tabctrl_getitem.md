---
UID: NF:commctrl.TabCtrl_GetItem
title: TabCtrl_GetItem macro
author: windows-sdk-content
description: Retrieves information about a tab in a tab control. You can use this macro or send the TCM_GETITEM message explicitly.
old-location: controls\TabCtrl_GetItem.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_getitem.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TabCtrl_GetItem, TabCtrl_GetItem macro [Windows Controls], _win32_TabCtrl_GetItem, _win32_TabCtrl_GetItem_cpp, commctrl/TabCtrl_GetItem, controls.TabCtrl_GetItem, controls._win32_TabCtrl_GetItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TabCtrl_GetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_GetItem macro


## -description


Retrieves information about a tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760589(v=VS.85).aspx">TCM_GETITEM</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the tab control. 


### -param iItem

Type: <b>int</b>

Index of the tab. 


### -param pitem

Type: <b>LPTCITEM</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb760554(v=VS.85).aspx">TCITEM</a> structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the 
					<b>mask</b> member specifies which attributes to return. If the <b>mask</b> member specifies the TCIF_TEXT value, the 
<b>pszText</b> member must contain the address of the buffer that receives the item text, and the <b>cchTextMax</b> member must specify the size of the buffer.


## -remarks



If the TCIF_TEXT flag is set in the 
				<b>mask</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb760554(v=VS.85).aspx">TCITEM</a> structure, the control may change the <b>pszText</b> member of the structure to point to the new text instead of filling the buffer with the requested text. The control may set the <b>pszText</b> member to <b>NULL</b> to indicate that no text is associated with the item.



