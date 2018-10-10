---
UID: NS:commctrl.tagNMLVSCROLL
title: tagNMLVSCROLL
author: windows-sdk-content
description: Provides information about a scrolling operation.
old-location: controls\NMLVSCROLL.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvscroll.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*LPNMLVSCROLL, LPNMLVSCROLL, LPNMLVSCROLL structure pointer [Windows Controls], NMLVSCROLL, NMLVSCROLL structure [Windows Controls], commctrl/LPNMLVSCROLL, commctrl/NMLVSCROLL, controls.NMLVSCROLL, controls.inet_NMLVSCROLL, inet_NMLVSCROLL, inet_NMLVSCROLL_cpp, tagNMLVSCROLL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
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
 - NMLVSCROLL
product: Windows
targetos: Windows
req.typenames: NMLVSCROLL, *LPNMLVSCROLL
req.redist: 
---

# tagNMLVSCROLL structure


## -description


Provides information about a scrolling operation.  



## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about a <a href="https://msdn.microsoft.com/2838dcd0-ac0f-48c7-94ba-dc36febedb94">LVN_ENDSCROLL</a> or a <a href="https://msdn.microsoft.com/67123db1-118c-43d7-8511-12a3c4413958">LVN_BEGINSCROLL</a> notification code. 


### -field dx

Type: <b>int</b>

Value of type <b>int</b> that specifies in pixels the horizontal position where a scrolling operation should begin or end. 


### -field dy

Type: <b>int</b>

Value of type <b>int</b> that specifies in pixels the vertical position where a scrolling operation should begin or end. 

