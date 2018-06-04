---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IViewObject::SetAdvise


## -description


Establishes a connection between the view object and an advise sink so that the advise sink can be notified about changes in the object's view.


## -parameters




### -param aspects [in]

View for which the advisory connection is being set up. Valid values are taken from the enumeration <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>. See the <b>DVASPECT</b> enumeration for more information.


### -param advf [in]

Contains a group of flags for controlling the advisory connection. Valid values are from the enumeration <a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a>. However, only some of the possible <b>ADVF</b> values are relevant for this method. The following table briefly describes the relevant values. See the <b>ADVF</b> enumeration for a more detailed description.

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
 

<div class="alert"><b>Note</b>  The ADVF_ONLYONCE and ADVF_PRIMEFIRST can be combined to provide an asynchronous call to <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. </div>
<div> </div>

### -param pAdvSink [in]

Pointer to the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface on the advisory sink that is to be informed of changes. A <b>NULL</b> value deletes any existing advisory connection.


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



A container application that is requesting a draw operation on a view object can also register with the <b>IViewObject::SetAdvise</b> method to be notified when the presentation of the view object changes. To find out about when an object's underlying data changes, you must call <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> separately.

To remove an existing advisory connection, call the <b>IViewObject::SetAdvise</b> method with <i>pAdvSink</i> set to <b>NULL</b>.

If the view object changes, a call is made to the appropriate advise sink through its <a href="https://msdn.microsoft.com/f2cb3a5b-826b-428a-9e92-e5d08880bddc">IAdviseSink::OnViewChange</a> method.

At any time, a given view object can support only one advisory connection. Therefore, when <b>IViewObject::SetAdvise</b> is called and the view object is already holding on to an advise sink pointer, OLE releases the existing pointer before the new one is registered.




## -see-also




<a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a>



<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>



<a href="https://msdn.microsoft.com/c56f6cbb-d2ea-4db4-a660-db8b7540ac94">IViewObject::GetAdvise</a>
 

 

