---
UID: NE:ocidl.tagPOINTERINACTIVE
title: tagPOINTERINACTIVE
author: windows-sdk-content
description: Indicate the activation policy of the object and are used in the IPointerInactive::GetActivationPolicy method.
old-location: com\pointerinactive.htm
tech.root: com
ms.assetid: b955af46-14bd-45b0-a4ef-b705e5d45a38
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: POINTERINACTIVE, POINTERINACTIVE enumeration [COM], POINTERINACTIVE_ACTIVATEONDRAG, POINTERINACTIVE_ACTIVATEONENTRY, POINTERINACTIVE_DEACTIVATEONLEAVE, _ctrl_POINTERINACTIVE, com.pointerinactive, ocidl/POINTERINACTIVE, ocidl/POINTERINACTIVE_ACTIVATEONDRAG, ocidl/POINTERINACTIVE_ACTIVATEONENTRY, ocidl/POINTERINACTIVE_DEACTIVATEONLEAVE, tagPOINTERINACTIVE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - OCIdl.h
api_name:
 - POINTERINACTIVE
product: Windows
targetos: Windows
req.typenames: POINTERINACTIVE
req.redist: 
---

# tagPOINTERINACTIVE enumeration


## -description


Indicate the activation policy of the object and are used in the <a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a> method.


## -enum-fields




### -field POINTERINACTIVE_ACTIVATEONENTRY

The object should be in-place activated when the mouse enters it during a mouse move operation.


### -field POINTERINACTIVE_DEACTIVATEONLEAVE

The object should be deactivated when the mouse leaves the object during a mouse move operation.


### -field POINTERINACTIVE_ACTIVATEONDRAG

The object should be in-place activated when the mouse is dragged over it during a drag and drop operation.


## -remarks



For more information on using the <b>POINTERINACTIVE_ACTIVATEONENTRY</b> and <b>POINTERINACTIVE_DEACTIVATEONLEAVE</b> values, see the <a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a> method.

<b>The POINTERINACTIVE_ACTIVATEONDRAG</b> value can be used to support drag and drop operations on an inactive object. An inactive object has no window to register itself as a potential drop target. Most containers ignore embedded, inactive objects as drop targets because of the overhead associated with activating them.

As an alternative to activating an object when the mouse pointer is over it during a drag and drop operation, the container can first <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to determine if the inactive object supports <a href="https://msdn.microsoft.com/dc08d512-6994-419a-a460-6274ce74e40f">IPointerInactive</a>. Then, if the object does not support IPointerInactive, the container can assume that it is not a drop target. If the object does support <b>IPointerInactive</b>, the container calls the <a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a> method. If the <b>POINTERINACTIVE_ACTIVATEONDRAG</b> value is set, the container activates the object in-place so the object can register its own <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface.

The container is processing its own <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> method when all these actions occur. To complete that method, the container returns <b>DROPEFFECT_NONE</b> for the <i>pdwEffect</i> parameter. Then, the drag and drop operation continues by calling the container's <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> and then calling the object's <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a>.


<div class="alert"><b>Important</b>  For windowless OLE objects this mechanism is slightly different. See I<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">OleInPlaceSiteWindowless</a> for more information on drag and drop operations for windowless objects.</div>
<div> </div>


If the drop occurs on the embedded object, the object is UI-activated and will get UI-deactivated when the focus changes again. If the drop does not occur on the object, the container should deactivate the object the next time it gets a call to its own <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a>. It is possible for the drop to occur on a third active object without an intervening call to the container's IDropTarget::DragEnter. In this case, the container should try to deactivate the object as soon as it can, for example, when it UI-activates another object.




## -see-also




<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>



<a href="https://msdn.microsoft.com/dc08d512-6994-419a-a460-6274ce74e40f">IPointerInactive</a>



<a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a>
 

 

