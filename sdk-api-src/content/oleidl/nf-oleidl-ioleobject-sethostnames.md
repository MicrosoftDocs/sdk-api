---
UID: NF:oleidl.IOleObject.SetHostNames
title: IOleObject::SetHostNames (oleidl.h)
description: Provides an object with the names of its container application and the compound document in which it is embedded.
helpviewer_keywords: ["IOleObject interface [COM]","SetHostNames method","IOleObject.SetHostNames","IOleObject::SetHostNames","SetHostNames","SetHostNames method [COM]","SetHostNames method [COM]","IOleObject interface","_ole_ioleobject_sethostnames","com.ioleobject_sethostnames","oleidl/IOleObject::SetHostNames"]
old-location: com\ioleobject_sethostnames.htm
tech.root: com
ms.assetid: 38cccb3d-e198-4996-991b-6c56451d25e3
ms.date: 12/05/2018
ms.keywords: IOleObject interface [COM],SetHostNames method, IOleObject.SetHostNames, IOleObject::SetHostNames, SetHostNames, SetHostNames method [COM], SetHostNames method [COM],IOleObject interface, _ole_ioleobject_sethostnames, com.ioleobject_sethostnames, oleidl/IOleObject::SetHostNames
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleObject::SetHostNames
 - oleidl/IOleObject::SetHostNames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.SetHostNames
---

# IOleObject::SetHostNames


## -description

Provides an object with the names of its container application and the compound document in which it is embedded.

## -parameters

### -param szContainerApp [in]

Pointer to the name of the container application in which the object is running.

### -param szContainerObj [in]

Pointer to the name of the compound document that contains the object. If you do not wish to display the name of the compound document, you can set this parameter to <b>NULL</b>.

## -returns

This method returns S_OK on success.

## -remarks

<h3><a id="Notes_for_Callers"></a><a id="notes_for_callers"></a><a id="NOTES_FOR_CALLERS"></a>Notes for Callers</h3>
Call <b>IOleObject::SetHostNames</b> only for embedded objects, because for linked objects, the link source provides its own separate editing window and title bar information.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An object's application of <b>IOleObject::SetHostNames</b> should include whatever modifications to its user interface may be appropriate to an object's embedded state. Such modifications typically will include adding and removing menu commands and altering the text displayed in the title bar of the editing window.

The complete window title for an embedded object in an SDI container application or an MDI application with a maximized child window should appear as follows:


``` syntax
<object application name> - <object short type> in <container document>
```

Otherwise, the title should be:


``` syntax
<object application name> - <container document>
```

The "object short type" refers to a form of an object's name short enough to be displayed in full in a list box. Because these identifying strings are not stored as part of the persistent state of the object, <b>IOleObject::SetHostNames</b> must be called each time the object loads or runs.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>
