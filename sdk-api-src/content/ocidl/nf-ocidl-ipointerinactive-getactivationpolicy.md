---
UID: NF:ocidl.IPointerInactive.GetActivationPolicy
title: IPointerInactive::GetActivationPolicy
author: windows-sdk-content
description: Retrieves the current activation policy for the object. This method is called by the container on receipt of a WM_SETCURSOR or WM_MOUSEMOVE message when an inactive object is under the mouse pointer.
old-location: com\ipointerinactive_getactivationpolicy.htm
old-project: com
ms.assetid: bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetActivationPolicy, GetActivationPolicy method [COM], GetActivationPolicy method [COM],IPointerInactive interface, IPointerInactive interface [COM],GetActivationPolicy method, IPointerInactive.GetActivationPolicy, IPointerInactive::GetActivationPolicy, _ctrl_ipointerinactive_getactivationpolicy, com.ipointerinactive_getactivationpolicy, ocidl/IPointerInactive::GetActivationPolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPointerInactive.GetActivationPolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPointerInactive::GetActivationPolicy


## -description


Retrieves the current activation policy for the object. This method is called by the container on receipt of a WM_SETCURSOR or WM_MOUSEMOVE message when an inactive object is under the mouse pointer.


## -parameters




### -param pdwPolicy [out]

A pointer to a variable that receives the activation policy. Possible values come from the <a href="https://msdn.microsoft.com/b955af46-14bd-45b0-a4ef-b705e5d45a38">POINTERINACTIVE</a> enumeration.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



The object can request to be in-place activated as soon as the mouse enters it through the POINTERINACTIVE_ACTIVATEONENTRY value. An object that provides more visual feedback than simply setting the mouse pointer would use this value. For example, if the object supports special visual feedback, it must enter the active state so it can draw the visual feedback that it supports.

An object can also use this method to request activation when the mouse is dragged over them during a drag and drop operation through the POINTERINACTIVE_ACTIVATEONDRAG.

If the object returns one of these values, the container should activate the object immediately and forward the Window message that triggered the call. The object then stays active and processes subsequent messages through its own window until the container gets another WM_SETCURSOR or WM_MOUSEMOVE. At this point, the container should deactivate the object.

For windowless OLE objects this mechanism is slightly different. See <a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a> for more information on drag and drop operations for windowless objects.

If the object returns both the POINTERINACTIVE_ACTIVATEONENTRY and the POINTERINACTIVE_DEACTIVATEONLEAVE values, the object is activated only when the mouse is over the object. If the POINTERINACTIVE_ACTIVATEONENTRY value alone is set, the object is activated once when the mouse first enters it, and it remains active.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The activation policy should not be cached. The container should call this method each time the mouse enters an inactive object.




## -see-also




<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>



<a href="https://msdn.microsoft.com/dc08d512-6994-419a-a460-6274ce74e40f">IPointerInactive</a>
 

 

