---
UID: NF:commctrl.ListView_MapIndexToID
title: ListView_MapIndexToID macro
author: windows-sdk-content
description: Maps the index of an item to a unique ID. You can use this macro or send the LVM_MAPINDEXTOID message explicitly.
old-location: controls\ListView_MapIndexToID.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_mapindextoid.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_MapIndexToID, ListView_MapIndexToID macro [Windows Controls], _win32_ListView_MapIndexToID, _win32_ListView_MapIndexToID_cpp, commctrl/ListView_MapIndexToID, controls.ListView_MapIndexToID, controls._win32_ListView_MapIndexToID
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
 - ListView_MapIndexToID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_MapIndexToID macro


## -description


Maps the index of an item to a unique ID. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761139(v=VS.85).aspx">LVM_MAPINDEXTOID</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param index

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A <b>UINT</b> that contains the index of an item.


## -remarks



List-view controls internally track items by index. This can present problems because indexes can change during the control's existence.

You can use this macro to tag an item with an ID when you create the item. You use this ID to guarantee uniqueness during the existence of the list-view control.   
		

To uniquely identify an item, take the index that is returned from a call such as <a href="https://msdn.microsoft.com/8143d11c-3740-4ffc-88f0-6df779c50521">IComponent::GetDisplayInfo</a> and call <a href="https://msdn.microsoft.com/en-us/library/Bb761139(v=VS.85).aspx">LVM_MAPINDEXTOID</a>. The return value is a unique ID.
		

<div class="alert"><b>Note</b>  In a multithreaded environment, you can only be sure the correct index is returned on the thread that hosts the list-view control, not on background threads.</div>
<div> </div>
To use <b>ListView_MapIndexToID</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



