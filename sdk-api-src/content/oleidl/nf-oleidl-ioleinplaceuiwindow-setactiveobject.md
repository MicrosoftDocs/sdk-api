---
UID: NF:oleidl.IOleInPlaceUIWindow.SetActiveObject
title: IOleInPlaceUIWindow::SetActiveObject (oleidl.h)
description: Provides a direct channel of communication between the object and each of the frame and document windows.
helpviewer_keywords: ["IOleInPlaceUIWindow interface [COM]","SetActiveObject method","IOleInPlaceUIWindow.SetActiveObject","IOleInPlaceUIWindow::SetActiveObject","SetActiveObject","SetActiveObject method [COM]","SetActiveObject method [COM]","IOleInPlaceUIWindow interface","_ole_ioleinplaceuiwindow_setactiveobject","com.ioleinplaceuiwindow_setactiveobject","oleidl/IOleInPlaceUIWindow::SetActiveObject"]
old-location: com\ioleinplaceuiwindow_setactiveobject.htm
tech.root: com
ms.assetid: 6ed1b09a-44e4-41dc-aa35-27efb3df66d6
ms.date: 12/05/2018
ms.keywords: IOleInPlaceUIWindow interface [COM],SetActiveObject method, IOleInPlaceUIWindow.SetActiveObject, IOleInPlaceUIWindow::SetActiveObject, SetActiveObject, SetActiveObject method [COM], SetActiveObject method [COM],IOleInPlaceUIWindow interface, _ole_ioleinplaceuiwindow_setactiveobject, com.ioleinplaceuiwindow_setactiveobject, oleidl/IOleInPlaceUIWindow::SetActiveObject
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
 - IOleInPlaceUIWindow::SetActiveObject
 - oleidl/IOleInPlaceUIWindow::SetActiveObject
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
 - IOleInPlaceUIWindow.SetActiveObject
---

# IOleInPlaceUIWindow::SetActiveObject


## -description

Provides a direct channel of communication between the object and each of the frame and document windows.

## -parameters

### -param pActiveObject [in]

A pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a> interface on the active in-place object.

### -param pszObjName [in]

A pointer to a string containing a name that describes the object an embedding container can use in composing its window title. It can be <b>NULL</b> if the object does not require the container to change its window titles. Containers should ignore this parameter and always use their own name in the title bar.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>

## -remarks

Generally, an embedded object should pass <b>NULL</b> for the <i>pszObjName</i> parameter (see Notes to Implementers below). However, if you are working in conjunction with a container that does display the name of the in-place active object in its title bar, then you should compose a string in the following form: &lt;<i>application name</i>&gt; – &lt;<i>object short-type name</i>&gt;.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
<b>IOleInPlaceUIWindow::SetActiveObject</b> is called by the object to establish a direct communication link between itself and the document and frame windows.

When deactivating, the object calls <b>IOleInPlaceUIWindow::SetActiveObject</b>, passing <b>NULL</b> for the <i>pActiveObject</i> and pszObjName parameters.

An object must call <b>IOleInPlaceUIWindow::SetActiveObject</b> before calling <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setmenu">IOleInPlaceFrame::SetMenu</a> to give the container the pointer to the active object. The container then uses this pointer in processing <b>IOleInPlaceFrame::SetMenu</b> and to pass to <a href="/windows/desktop/api/ole2/nf-ole2-olesetmenudescriptor">OleSetMenuDescriptor</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The Microsoft Windows User Interface Design Guide recommends that an in-place container ignore the <i>pszObjName</i> parameter passed in this method. The guide says "The title bar is not affected by in-place activation. It always displays the top-level container's name."

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-setmenu">IOleInPlaceFrame::SetMenu</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow">IOleInPlaceUIWindow</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetmenudescriptor">OleSetMenuDescriptor</a>