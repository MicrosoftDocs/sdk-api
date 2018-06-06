---
UID: NF:commctrl.ListView_SubItemHitTestEx
title: ListView_SubItemHitTestEx macro
author: windows-sdk-content
description: Determines which list-view item or subitem is located at a given position. You can use this macro or send the LVM_SUBITEMHITTEST message explicitly.
old-location: controls\ListView_SubItemHitTestEx.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_subitemhittestex.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListView_SubItemHitTestEx, ListView_SubItemHitTestEx macro [Windows Controls], _shell_ListView_SubItemHitTestEx, _shell_ListView_SubItemHitTestEx_cpp, commctrl/ListView_SubItemHitTestEx, controls.ListView_SubItemHitTestEx, controls._shell_ListView_SubItemHitTestEx
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
 - ListView_SubItemHitTestEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SubItemHitTestEx macro


## -description


Determines which list-view item or subitem is located at a given position. You can use this macro or send the <a href="https://msdn.microsoft.com/1468febb-af0d-4c04-b0b1-cda5ec77aa2c">LVM_SUBITEMHITTEST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control that will be hit-tested. 


### -param plvhti

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/1906cc92-e6e6-470c-86d5-042578833391">LVHITTESTINFO</a> structure. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure within <b>LVHITTESTINFO</b> must be set to the client coordinates to be hit-tested. 


## -remarks



This macro passes -1 as the <i>wparam</i> of the message, specifying that the <b>iGroup</b> member of <i>plvhti</i> is retrieved.
	



