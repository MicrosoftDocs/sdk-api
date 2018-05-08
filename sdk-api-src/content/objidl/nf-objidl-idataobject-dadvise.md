---
UID: NF:objidl.IDataObject.DAdvise
title: IDataObject::DAdvise
author: windows-driver-content
description: Called by an object supporting an advise sink to create a connection between a data object and the advise sink. This enables the advise sink to be notified of changes in the data of the object.
old-location: com\idataobject_dadvise.htm
old-project: com
ms.assetid: be9891d4-aad3-42a0-8c8e-4b86091ff03b
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: DAdvise, DAdvise method [COM], DAdvise method [COM],IDataObject interface, IDataObject interface [COM],DAdvise method, IDataObject.DAdvise, IDataObject::DAdvise, _ole_idataobject_dadvise, com.idataobject_dadvise, objidl/IDataObject::DAdvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IDataObject.DAdvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataObject::DAdvise


## -description


Called by an object supporting an advise sink to create a connection between a data object and the advise sink. This enables the advise sink to be notified of changes in the data of the object.


## -parameters




### -param pformatetc [in]

A pointer to a <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure that defines the format, target device, aspect, and medium that will be used for future notifications. For example, one sink may want to know only when the bitmap representation of the data in the data object changes. Another sink may be interested in only the metafile format of the same object. Each advise sink is notified when the data of interest changes. This data is passed back to the advise sink when notification occurs.


### -param advf [in]

A group of flags for controlling the advisory connection. Possible values are from the <a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a> enumeration. However, only some of the possible <b>ADVF</b> values are relevant for this method. The following table briefly describes the relevant values.

<table>
<tr>
<th>ADVF Value</th>
<th>Description</th>
</tr>
<tr>
<td>ADVF_NODATA
</td>
<td>
Asks the data object to avoid sending data with the notifications. Typically data is sent. This flag is a way to override the default behavior. When ADVF_NODATA is used, the <b>tymed</b> member of the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> structure that is passed to <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">OnDataChange</a> will usually contain TYMED_NULL. The caller can then retrieve the data with a subsequent <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> call.

</td>
</tr>
<tr>
<td>ADVF_ONLYONCE
</td>
<td>
Causes the advisory connection to be destroyed after the first change notification is sent. An implicit call to <a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">IDataObject::DUnadvise</a> is made on behalf of the caller to remove the connection.

</td>
</tr>
<tr>
<td>ADVF_PRIMEFIRST
</td>
<td>
Asks for an additional initial notification. The combination of ADVF_ONLYONCE and ADVF_PRIMEFIRST provides, in effect, an asynchronous <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> call.

</td>
</tr>
<tr>
<td>ADVF_DATAONSTOP
</td>
<td>
When specified with ADVF_NODATA, this flag causes a last notification with the data included to to be sent before the data object is destroyed.

If used without ADVF_NODATA, <b>DAdvise</b> can be implemented in one of the following ways:

<ul>
<li>The ADVF_DATAONSTOP can be ignored.</li>
<li>The object can behave as if ADVF_NODATA was specified.</li>
</ul>
A change notification is sent only in the shutdown case. Data changes prior to shutdown do not cause a notification to be sent.

</td>
</tr>
</table>
 


### -param pAdvSink [in]

A pointer to the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface on the advisory sink that will receive the change notification.


### -param pdwConnection [out]

A token that identifies this connection. You can use this token later to delete the advisory connection (by passing it to <a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">IDataObject::DUnadvise</a>). If this value is 0, the connection was not established.


## -returns



This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented on the data object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
The value for <b>lindex</b> is not valid; currently, only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>pformatetc</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_ADVISENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The data object does not support change notification.

</td>
</tr>
</table>
 




## -remarks



<b>DAdvise</b> creates a change notification connection between a data object and the caller. The caller provides an advisory sink to which the notifications can be sent when the object's data changes.

Objects used simply for data transfer typically do not support advisory notifications and return OLE_E_ADVISENOTSUPPORTED from <b>DAdvise</b>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The object supporting the advise sink calls <b>DAdvise</b> to set up the connection, specifying the format, aspect, medium, and/or target device of interest in the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure passed in. If the data object does not support one or more of the requested attributes or the sending of notifications at all, it can refuse the connection by returning OLE_E_ADVISENOTSUPPORTED.

Containers of linked objects can set up advisory connections directly with the bound link source or indirectly through the standard OLE link object that manages the connection. Connections set up with the bound link source are not automatically deleted. The container must explicitly call <a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">IDataObject::DUnadvise</a> on the bound link source to delete an advisory connection. The OLE link object, manipulated through the <a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a> interface, is implemented in the default handler. Connections set up through the OLE link object are destroyed when the link object is deleted.

The OLE default link object creates a "wildcard advise" with the link source so OLE can maintain the time of last change. This advise is specifically used to note the time that anything changed. OLE ignores all data formats that may have changed, noting only the time of last change. To allow wildcard advises, set the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> members as follows before calling <b>DAdvise</b>:

<pre class="syntax" xml:space="preserve"><code>cf == 0; 
ptd == NULL; 
dwAspect == -1; 
lindex == -1 
tymed == -1;</code></pre>
The advise flags should also include ADVF_NODATA. Wildcard advises from OLE should always be accepted by applications.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
To simplify the implementation of <b>DAdvise</b> and the other notification methods in <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> (<a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">DUnadvise</a> and <a href="https://msdn.microsoft.com/319637fd-d9b5-4da0-ac92-4c52fa9f5231">EnumDAdvise</a>) that supports notification, OLE provides an advise holder object that manages the registration and sending of notifications. To get a pointer to this object, call the helper function <a href="https://msdn.microsoft.com/a2114f2f-106a-4a26-ba94-1b40af90a0f3">CreateDataAdviseHolder</a> on the first invocation of <b>DAdvise</b>. This supplies a pointer to the object's <a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a> interface. Then, delegate the call to the <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">IDataAdviseHolder::Advise</a> method in the data advise holder, which creates, and subsequently manages, the requested connection.





## -see-also




<a href="https://msdn.microsoft.com/a2114f2f-106a-4a26-ba94-1b40af90a0f3">CreateDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>
 

 

