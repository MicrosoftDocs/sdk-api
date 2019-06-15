---
UID: NF:commctrl.ListView_GetFooterInfo
title: ListView_GetFooterInfo macro (commctrl.h)
author: windows-sdk-content
description: Gets information on the footer of a specified list-view control. Use this macro or send the LVM_GETFOOTERINFO message explicitly.
old-location: controls\ListView_GetFooterInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfooterinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_GetFooterInfo, ListView_GetFooterInfo macro [Windows Controls], _shell_ListView_GetFooterInfo, _shell_ListView_GetFooterInfo_cpp, commctrl/ListView_GetFooterInfo, controls.ListView_GetFooterInfo, controls._shell_ListView_GetFooterInfo
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
 - ListView_GetFooterInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetFooterInfo macro


## -description


Gets information on the footer of a specified list-view control. Use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getfooterinfo">LVM_GETFOOTERINFO</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.


### -param plvfi [in, out]

Type: <b>LPLVFOOTERINFO</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-taglvfooterinfo">LVFOOTERINFO</a> structure to receive information depending on the value of the <b>mask</b> member. The calling application is responsible for allocating this structure and setting the <b>mask</b> member.

