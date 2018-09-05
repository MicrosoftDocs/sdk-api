---
UID: NF:oleidl.IOleObject.SetExtent
title: IOleObject::SetExtent
author: windows-sdk-content
description: Informs an object of how much display space its container has assigned it.
old-location: com\ioleobject_setextent.htm
old-project: com
ms.assetid: f1960095-7c9a-4058-aef1-f31e3d6e3509
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOleObject interface [COM],SetExtent method, IOleObject.SetExtent, IOleObject::SetExtent, SetExtent, SetExtent method [COM], SetExtent method [COM],IOleObject interface, _ole_ioleobject_setextent, com.ioleobject_setextent, oleidl/IOleObject::SetExtent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.SetExtent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleObject::SetExtent


## -description


Informs an object of how much display space its container has assigned it.


## -parameters




### -param dwDrawAspect [in]

DWORD that describes which form, or "aspect," of an object is to be displayed. The object's container obtains this value from the enumeration <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> (refer to the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> enumeration). The most common aspect is DVASPECT_CONTENT, which specifies a full rendering of the object within its container. An object can also be rendered as an icon, a thumbnail version for display in a browsing tool, or a print version, which displays the object as it would be rendered using the <b>File Print</b> command.


### -param psizel [in]

Pointer to the size limit for the object.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object is not running.

</td>
</tr>
</table>
 




## -remarks



A container calls <b>IOleObject::SetExtent</b> when it needs to dictate to an embedded object the size at which it will be displayed. Often, this call occurs in response to an end user resizing the object window. Upon receiving the call, the object, if possible, should recompose itself gracefully to fit the new window.

Whenever possible, a container seeks to display an object at its finest resolution, sometimes called the object's native size. All objects, however, have a default display size specified by their applications, and in the absence of other constraints, this is the size they will use to display themselves. Since an object knows its optimum display size better than does its container, the latter normally requests that size from a running object by calling <b>IOleObject::SetExtent</b>. Only in cases where the container cannot accommodate the value returned by the object does it override the object's preference by calling <b>IOleObject::SetExtent</b>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You can call <b>IOleObject::SetExtent</b> on an object only when the object is running. If a container resizes an object while an object is not running, the container should keep track of the object's new size but defer calling <b>IOleObject::SetExtent</b> until a user activates the object. If the OLEMISC_RECOMPOSEONRESIZE bit is set on an object, its container should force the object to run before calling <b>IOleObject::SetExtent</b>.

As noted above, a container may want to delegate responsibility for setting the size of an object's display site to the object itself, by calling <b>IOleObject::SetExtent</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You may want to implement this method so that your object rescales itself to match as closely as possible the maximum space available to it in its container.

If an object's size is fixed, that is, if it cannot be set by its container, <b>IOleObject::SetExtent</b> should return E_FAIL. This is always the case with linked objects, whose sizes are set by their link sources, not by their containers.




## -see-also




<a href="https://msdn.microsoft.com/f2cb3a5b-826b-428a-9e92-e5d08880bddc">IAdviseSink::OnViewChange</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/babaf55e-6c43-48d8-ad13-1333e29a3e1d">IOleObject::GetExtent</a>



<a href="https://msdn.microsoft.com/66eedee0-58b5-4676-93db-599ed19a02b6">IViewObject2::GetExtent</a>
 

 

