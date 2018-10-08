---
UID: NF:commctrl.ListView_GetGroupHeaderImageList
title: ListView_GetGroupHeaderImageList macro
author: windows-sdk-content
description: Gets the group header image list that has been set for an existing list-view control.
old-location: controls\ListView_GetGroupHeaderImageList.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupheaderimagelist.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ListView_GetGroupHeaderImageList, ListView_GetGroupHeaderImageList macro [Windows Controls], _shell_ListView_GetGroupHeaderImageList, _shell_ListView_GetGroupHeaderImageList_cpp, commctrl/ListView_GetGroupHeaderImageList, controls.ListView_GetGroupHeaderImageList, controls._shell_ListView_GetGroupHeaderImageList
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
 - ListView_GetGroupHeaderImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetGroupHeaderImageList macro


## -description


Gets the group header image list that has been set for an existing list-view control.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control.


## -remarks



To specify an image list another way, such as, by large icons, small icons, or state images, send the <a href="https://msdn.microsoft.com/en-us/library/Bb774943(v=VS.85).aspx">LVM_GETIMAGELIST</a> message explicitly.



