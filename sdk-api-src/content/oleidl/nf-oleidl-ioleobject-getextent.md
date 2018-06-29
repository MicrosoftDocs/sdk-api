---
UID: NF:oleidl.IOleObject.GetExtent
title: IOleObject::GetExtent
author: windows-sdk-content
description: Retrieves a running object's current display size.
old-location: com\ioleobject_getextent.htm
old-project: com
ms.assetid: babaf55e-6c43-48d8-ad13-1333e29a3e1d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: GetExtent, GetExtent method [COM], GetExtent method [COM],IOleObject interface, IOleObject interface [COM],GetExtent method, IOleObject.GetExtent, IOleObject::GetExtent, _ole_ioleobject_getextent, com.ioleobject_getextent, oleidl/IOleObject::GetExtent
ms.prod: windows
ms.technology: windows-sdk
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
 - IOleObject.GetExtent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleObject::GetExtent


## -description


Retrieves a running object's current display size.


## -parameters




### -param dwDrawAspect [in]

The aspect of the object whose limit is to be retrieved; the value is obtained from the enumerations <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> and from <a href="https://msdn.microsoft.com/9000b807-5a42-437f-a3e8-a7b23be1665b">DVASPECT2</a>. Note that newer objects and containers that support optimized drawing interfaces support the <b>DVASPECT2</b> enumeration values. Older objects and containers that do not support optimized drawing interfaces may not support <b>DVASPECT2</b>. The most common value for this method is DVASPECT_CONTENT, which specifies a full rendering of the object within its container.


### -param psizel [out]

Pointer to where the object's size is to be returned.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <i>dwDrawAspect</i> value is invalid.

</td>
</tr>
</table>
 




## -remarks



A container calls <b>IOleObject::GetExtent</b> on a running object to retrieve its current display size. If the container can accommodate that size, it will normally do so because the object, after all, knows what size it should be better than the container does. A container normally makes this call as part of initializing an object.

The display size returned by <b>IOleObject::GetExtent</b> may differ from the size last set by <a href="https://msdn.microsoft.com/f1960095-7c9a-4058-aef1-f31e3d6e3509">IOleObject::SetExtent</a> because the latter method dictates the object's display space at the time the method is called but does not necessarily change the object's native size, as determined by its application.

If one of the new aspects is requested in <i>dwAspect</i>, this method can either fail or return the same rectangle as for the DVASPECT_CONTENT aspect.

<div class="alert"><b>Note</b>  This method must return the same size as DVASPECT_CONTENT for all the new aspects in <a href="https://msdn.microsoft.com/9000b807-5a42-437f-a3e8-a7b23be1665b">DVASPECT2</a>. <a href="https://msdn.microsoft.com/66eedee0-58b5-4676-93db-599ed19a02b6">IViewObject2::GetExtent</a> must do the same thing.</div>
<div> </div>
<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Because a container can make this call only to a running object, the container must instead call <a href="https://msdn.microsoft.com/66eedee0-58b5-4676-93db-599ed19a02b6">IViewObject2::GetExtent</a> if it wants to get the display size of a loaded object from its cache.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementation consists of filling the sizel structure with an object's height and width.




## -see-also




<a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>



<a href="https://msdn.microsoft.com/9000b807-5a42-437f-a3e8-a7b23be1665b">DVASPECT2</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/babaf55e-6c43-48d8-ad13-1333e29a3e1d">IOleObject::GetExtent</a>



<a href="https://msdn.microsoft.com/f1960095-7c9a-4058-aef1-f31e3d6e3509">IOleObject::SetExtent</a>
 

 

