---
UID: NF:commctrl.ListView_SetGroupHeaderImageList
title: ListView_SetGroupHeaderImageList macro (commctrl.h)
author: windows-sdk-content
description: Assigns an image list to the group header of a list-view control.
old-location: controls\ListView_SetGroupHeaderImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupheaderimagelist.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_SetGroupHeaderImageList, ListView_SetGroupHeaderImageList macro [Windows Controls], _shell_ListView_SetGroupHeaderImageList, _shell_ListView_SetGroupHeaderImageList_cpp, commctrl/ListView_SetGroupHeaderImageList, controls.ListView_SetGroupHeaderImageList, controls._shell_ListView_SetGroupHeaderImageList
ms.topic: macro
f1_keywords: ["commctrl/ListView_SetGroupHeaderImageList"]
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
 - ListView_SetGroupHeaderImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetGroupHeaderImageList macro


## -description


Assigns an image list to the group header of a list-view control.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.


### -param himl [in]

Type: <b>HIML</b>

A handle to the image list.


## -remarks



The current image list will be destroyed when the list-view control is destroyed unless the <a href="https://docs.microsoft.com/windows/desktop/Controls/list-view-window-styles">LVS_SHAREIMAGELISTS</a> style is set. If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.



