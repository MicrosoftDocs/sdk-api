---
UID: NS:richedit._enoleopfailed
title: ENOLEOPFAILED (richedit.h)
description: Contains information about a failed operation.
old-location: controls\ENOLEOPFAILED.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\enoleopfailed.htm
ms.date: 12/05/2018
ms.keywords: ENOLEOPFAILED, ENOLEOPFAILED structure [Windows Controls], _win32_ENOLEOPFAILED_str, _win32_ENOLEOPFAILED_str_cpp, controls.ENOLEOPFAILED, controls._win32_ENOLEOPFAILED_str, richedit/ENOLEOPFAILED
f1_keywords:
- richedit/ENOLEOPFAILED
dev_langs:
- c++
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
- ENOLEOPFAILED
targetos: Windows
req.typenames: ENOLEOPFAILED
req.redist: 
ms.custom: 19H1
---

# ENOLEOPFAILED structure


## -description


Contains information about a failed operation.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> notification header. 


### -field iob

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Object index.


### -field lOper

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Operation that failed. This can be <b>OLEOP_DOVERB</b> to indicate that <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a> failed. 


### -field hr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Error code returned by the object on the operation. 


## -see-also




<a href="https://msdn.microsoft.com/b674c36f-2454-473e-8e1c-368c0afd8c34">EN_OLEOPFAILED</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a>



<b>Other Resources</b>



<b>Reference</b>
 

 

