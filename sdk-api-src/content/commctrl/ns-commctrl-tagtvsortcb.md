---
UID: NS:commctrl.tagTVSORTCB
title: tagTVSORTCB
author: windows-sdk-content
description: Contains information used to sort child items in a tree-view control. This structure is used with the TVM_SORTCHILDRENCB message. This structure is identical to the TV_SORTCB structure, but it has been renamed to follow current naming conventions.
old-location: controls\TVSORTCB.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\structures\tvsortcb.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*LPTVSORTCB, LPTVSORTCB, LPTVSORTCB structure pointer [Windows Controls], TVSORTCB, TVSORTCB structure [Windows Controls], _win32_TVSORTCB, _win32_TVSORTCB_cpp, commctrl/LPTVSORTCB, commctrl/TVSORTCB, controls.TVSORTCB, controls._win32_TVSORTCB, tagTVSORTCB"
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
 - TVSORTCB
product: Windows
targetos: Windows
req.typenames: TVSORTCB, *LPTVSORTCB
req.redist: 
---

# tagTVSORTCB structure


## -description


Contains information used to sort child items in a tree-view control. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb773785(v=VS.85).aspx">TVM_SORTCHILDRENCB</a> message. This structure is identical to the 
			<b>TV_SORTCB</b> structure, but it has been renamed to follow current naming conventions. 


## -struct-fields




### -field hParent

Type: <b>HTREEITEM</b>

Handle to the parent item. 


### -field lpfnCompare

Type: <b>PFNTVCOMPARE</b>

Address of an application-defined callback function, which is called during a sort operation each time the relative order of two list items needs to be compared. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPARAM</a></b>

Application-defined value that gets passed as the 
					<i>lParamSort</i> argument in the callback function specified in 
					<b>lpfnCompare</b>. 


## -remarks



The callback function specified by <b>lpfnCompare</b> has the following form:


<pre class="syntax" xml:space="preserve"><code>
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
</code></pre>
The callback function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.

The <i>lParam1</i> and <i>lParam2</i> parameters correspond to the lParam member of the <a href="https://msdn.microsoft.com/en-us/library/Bb773456(v=VS.85).aspx">TVITEM</a> structure for the two items being compared. The <i>lParamSort</i> parameter corresponds to the <b>lParam</b> member of this structure.



