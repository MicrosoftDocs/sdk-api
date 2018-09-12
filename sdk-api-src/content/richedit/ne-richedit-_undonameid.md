---
UID: NE:richedit._undonameid
title: "_undonameid"
author: windows-sdk-content
description: Contains values that indicate types of rich edit control actions that can be undone or redone. The EM_GETREDONAME and EM_GETUNDONAME messages use this enumeration type to return a value.
old-location: controls\UNDONAMEID.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditenumerationtypes\undonameid.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UID_AUTOTABLE, UID_CUT, UID_DELETE, UID_DRAGDROP, UID_PASTE, UID_TYPING, UID_UNKNOWN, UNDONAMEID, UNDONAMEID enumeration [Windows Controls], _undonameid, _win32_UNDONAMEID_str, _win32_UNDONAMEID_str_cpp, controls.UNDONAMEID, controls._win32_UNDONAMEID_str, richedit/UID_AUTOTABLE, richedit/UID_CUT, richedit/UID_DELETE, richedit/UID_DRAGDROP, richedit/UID_PASTE, richedit/UID_TYPING, richedit/UID_UNKNOWN, richedit/UNDONAMEID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: richedit.h
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
 - Richedit.h
api_name:
 - UNDONAMEID
product: Windows
targetos: Windows
req.typenames: UNDONAMEID
req.redist: 
---

# _undonameid enumeration


## -description


Contains values that indicate types of rich edit control actions that can be undone or redone. The <a href="https://msdn.microsoft.com/8649236f-32dc-45d3-847e-c9f65ffba44c">EM_GETREDONAME</a> and <a href="https://msdn.microsoft.com/43351909-f8bc-425a-9d9b-655e3b47eb75">EM_GETUNDONAME</a> messages use this enumeration type to return a value. 


## -enum-fields




### -field UID_UNKNOWN

The type of undo action is unknown. 


### -field UID_TYPING

Typing operation. 


### -field UID_DELETE

Delete operation. 


### -field UID_DRAGDROP

Drag-and-drop operation. 


### -field UID_CUT

Cut operation. 


### -field UID_PASTE

Paste operation. 


### -field UID_AUTOTABLE

Automatic table insertion; for example, typing +---+---+&lt;Enter&gt; to insert a table row. 



## -see-also




<a href="https://msdn.microsoft.com/8649236f-32dc-45d3-847e-c9f65ffba44c">EM_GETREDONAME</a>



<a href="https://msdn.microsoft.com/43351909-f8bc-425a-9d9b-655e3b47eb75">EM_GETUNDONAME</a>



<b>Reference</b>
 

 

