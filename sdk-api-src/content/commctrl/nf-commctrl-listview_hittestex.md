---
UID: NF:commctrl.ListView_HitTestEx
title: ListView_HitTestEx macro (commctrl.h)
author: windows-sdk-content
description: Determines which list-view item, if any, is at a specified position. You can use this macro or send the LVM_HITTEST message explicitly.
old-location: controls\ListView_HitTestEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_hittestex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_HitTestEx, ListView_HitTestEx macro [Windows Controls], _shell_ListView_HitTestEx, _shell_ListView_HitTestEx_cpp, commctrl/ListView_HitTestEx, controls.ListView_HitTestEx, controls._shell_ListView_HitTestEx
ms.topic: macro
f1_keywords: 
 - "commctrl/ListView_HitTestEx"
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
 - ListView_HitTestEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_HitTestEx macro


## -description


Determines which list-view item, if any, is at a specified position. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-hittest">LVM_HITTEST</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param pinfo

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvhittestinfo">LVHITTESTINFO</a> structure that contains the position to hit test and receives information about the results of the hit test. 


## -remarks



This macro passes -1 as the <i>wParam</i> of the message, specifying that the <b>iGroup</b> and <b>iSubItem</b> members of <i>pinfo</i> are retrieved.
	



