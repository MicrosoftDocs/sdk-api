---
UID: NF:commctrl.ListView_HitTestEx
title: ListView_HitTestEx macro
author: windows-sdk-content
description: Determines which list-view item, if any, is at a specified position. You can use this macro or send the LVM_HITTEST message explicitly.
old-location: controls\ListView_HitTestEx.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_hittestex.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ListView_HitTestEx, ListView_HitTestEx macro [Windows Controls], _shell_ListView_HitTestEx, _shell_ListView_HitTestEx_cpp, commctrl/ListView_HitTestEx, controls.ListView_HitTestEx, controls._shell_ListView_HitTestEx
ms.prod: windows
ms.technology: windows-sdk
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
 - ListView_HitTestEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_HitTestEx macro


## -description


Determines which list-view item, if any, is at a specified position. You can use this macro or send the <a href="https://msdn.microsoft.com/81df4ed1-30bd-4b63-9cb9-5163cb7cf52c">LVM_HITTEST</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param pinfo

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/1906cc92-e6e6-470c-86d5-042578833391">LVHITTESTINFO</a> structure that contains the position to hit test and receives information about the results of the hit test. 


## -remarks



This macro passes -1 as the <i>wParam</i> of the message, specifying that the <b>iGroup</b> and <b>iSubItem</b> members of <i>pinfo</i> are retrieved.
	



