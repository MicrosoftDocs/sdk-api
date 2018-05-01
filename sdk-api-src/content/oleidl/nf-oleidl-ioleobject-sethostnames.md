---
UID: NF:oleidl.IOleObject.SetHostNames
title: IOleObject::SetHostNames method
author: windows-driver-content
description: Provides an object with the names of its container application and the compound document in which it is embedded.
old-location: com\ioleobject_sethostnames.htm
old-project: com
ms.assetid: 38cccb3d-e198-4996-991b-6c56451d25e3
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IOleObject, IOleObject interface [COM], SetHostNames method, IOleObject::SetHostNames, SetHostNames method [COM], SetHostNames method [COM], IOleObject interface, SetHostNames,IOleObject.SetHostNames, _ole_ioleobject_sethostnames, com.ioleobject_sethostnames, oleidl/IOleObject::SetHostNames
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleObject.SetHostNames
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleObject::SetHostNames method


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

<pre class="syntax" xml:space="preserve"><code>&lt;object application name&gt; - &lt;object short type&gt; in &lt;container document&gt;</code></pre>
Otherwise, the title should be:

<pre class="syntax" xml:space="preserve"><code>&lt;object application name&gt; - &lt;container document&gt;</code></pre>
The "object short type" refers to a form of an object's name short enough to be displayed in full in a list box. Because these identifying strings are not stored as part of the persistent state of the object, <b>IOleObject::SetHostNames</b> must be called each time the object loads or runs.




## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a>
 

 

