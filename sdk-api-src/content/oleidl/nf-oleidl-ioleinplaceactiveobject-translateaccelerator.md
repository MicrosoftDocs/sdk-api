---
UID: NF:oleidl.IOleInPlaceActiveObject.TranslateAccelerator
title: IOleInPlaceActiveObject::TranslateAccelerator (oleidl.h)
description: Processes menu accelerator-key messages from the container's message queue. This method should only be used for objects created by a DLL object application.
helpviewer_keywords: ["IOleInPlaceActiveObject interface [COM]","TranslateAccelerator method","IOleInPlaceActiveObject.TranslateAccelerator","IOleInPlaceActiveObject::TranslateAccelerator","TranslateAccelerator","TranslateAccelerator method [COM]","TranslateAccelerator method [COM]","IOleInPlaceActiveObject interface","_ole_ioleinplaceactiveobject_translateaccelerator","com.ioleinplaceactiveobject_translateaccelerator","oleidl/IOleInPlaceActiveObject::TranslateAccelerator"]
old-location: com\ioleinplaceactiveobject_translateaccelerator.htm
tech.root: com
ms.assetid: ce460c52-c7aa-4ee4-955e-76407af7cf1e
ms.date: 12/05/2018
ms.keywords: IOleInPlaceActiveObject interface [COM],TranslateAccelerator method, IOleInPlaceActiveObject.TranslateAccelerator, IOleInPlaceActiveObject::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM],IOleInPlaceActiveObject interface, _ole_ioleinplaceactiveobject_translateaccelerator, com.ioleinplaceactiveobject_translateaccelerator, oleidl/IOleInPlaceActiveObject::TranslateAccelerator
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
 - IOleInPlaceActiveObject::TranslateAccelerator
 - oleidl/IOleInPlaceActiveObject::TranslateAccelerator
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
 - IOleInPlaceActiveObject.TranslateAccelerator
---

# IOleInPlaceActiveObject::TranslateAccelerator


## -description

Processes menu accelerator-key messages from the container's message queue. This method should only be used for objects created by a DLL object application.

## -parameters

### -param lpmsg [in]

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure for the message that might need to be translated.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The message was not translated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter values are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
IThere is insufficient memory available for the operation.

</td>
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

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Active in-place objects must always be given the first chance at translating accelerator keystrokes. You can provide this opportunity by calling <b>IOleInPlaceActiveObject::TranslateAccelerator</b> from your container's message loop before doing any other translation. You should apply your own translation only when this method returns S_FALSE.

If you call <b>IOleInPlaceActiveObject::TranslateAccelerator</b> for an object that is not created by a DLL object application, the default object handler returns S_FALSE.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An object created by an EXE object application gets keystrokes from its own message pump, so the container does not get those messages.

If you need to implement this method, you can do so by simply wrapping the call to the <a href="/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a> function.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceactiveobject">IOleInPlaceActiveObject</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oletranslateaccelerator">OleTranslateAccelerator</a>



<a href="/windows/desktop/DirectShow/cbasepropertypage-translateaccelerator">TranslateAccelerator</a>