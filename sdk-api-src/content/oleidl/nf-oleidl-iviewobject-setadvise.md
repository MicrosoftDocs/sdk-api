---
UID: NF:oleidl.IViewObject.SetAdvise
title: IViewObject::SetAdvise (oleidl.h)
description: Establishes a connection between the view object and an advise sink so that the advise sink can be notified about changes in the object's view.
helpviewer_keywords: ["ADVF_ONLYONCE","ADVF_PRIMEFIRST","IViewObject interface [COM]","SetAdvise method","IViewObject.SetAdvise","IViewObject::SetAdvise","SetAdvise","SetAdvise method [COM]","SetAdvise method [COM]","IViewObject interface","_ole_iviewobject_setadvise","com.iviewobject_setadvise","oleidl/IViewObject::SetAdvise"]
old-location: com\iviewobject_setadvise.htm
tech.root: com
ms.assetid: 64712679-8454-41fa-9497-f0ab97240a51
ms.date: 12/05/2018
ms.keywords: ADVF_ONLYONCE, ADVF_PRIMEFIRST, IViewObject interface [COM],SetAdvise method, IViewObject.SetAdvise, IViewObject::SetAdvise, SetAdvise, SetAdvise method [COM], SetAdvise method [COM],IViewObject interface, _ole_iviewobject_setadvise, com.iviewobject_setadvise, oleidl/IViewObject::SetAdvise
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
 - IViewObject::SetAdvise
 - oleidl/IViewObject::SetAdvise
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
 - IViewObject.SetAdvise
---

# IViewObject::SetAdvise


## -description

Establishes a connection between the view object and an advise sink so that the advise sink can be notified about changes in the object's view.

## -parameters

### -param aspects [in]

View for which the advisory connection is being set up. Valid values are taken from the enumeration <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>. See the <b>DVASPECT</b> enumeration for more information.

### -param advf [in]

Contains a group of flags for controlling the advisory connection. Valid values are from the enumeration <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a>. However, only some of the possible <b>ADVF</b> values are relevant for this method. The following table briefly describes the relevant values. See the <b>ADVF</b> enumeration for a more detailed description.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADVF_ONLYONCE"></a><a id="advf_onlyonce"></a><dl>
<dt><b>ADVF_ONLYONCE</b></dt>
</dl>
</td>
<td width="60%">
Causes the advisory connection to be destroyed after the first notification is sent.

</td>
</tr>
<tr>
<td width="40%"><a id="ADVF_PRIMEFIRST"></a><a id="advf_primefirst"></a><dl>
<dt><b>ADVF_PRIMEFIRST</b></dt>
</dl>
</td>
<td width="60%">
Causes an initial notification to be sent regardless of whether data has changed from its current state.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The ADVF_ONLYONCE and ADVF_PRIMEFIRST can be combined to provide an asynchronous call to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>. </div>
<div> </div>

### -param pAdvSink [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface on the advisory sink that is to be informed of changes. A <b>NULL</b> value deletes any existing advisory connection.

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
<dt><b>OLE_E_ADVISENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Advisory notifications are not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>dwAspect</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the supplied values is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

A container application that is requesting a draw operation on a view object can also register with the <b>IViewObject::SetAdvise</b> method to be notified when the presentation of the view object changes. To find out about when an object's underlying data changes, you must call <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> separately.

To remove an existing advisory connection, call the <b>IViewObject::SetAdvise</b> method with <i>pAdvSink</i> set to <b>NULL</b>.

If the view object changes, a call is made to the appropriate advise sink through its <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onviewchange">IAdviseSink::OnViewChange</a> method.

At any time, a given view object can support only one advisory connection. Therefore, when <b>IViewObject::SetAdvise</b> is called and the view object is already holding on to an advise sink pointer, OLE releases the existing pointer before the new one is registered.

## -see-also

<a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-getadvise">IViewObject::GetAdvise</a>