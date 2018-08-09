---
UID: NN:objidl.IDataObject
title: IDataObject
author: windows-sdk-content
description: Enables data transfer and notification of changes in data.
old-location: com\idataobject.htm
old-project: com
ms.assetid: 8a002deb-2727-456c-8078-a9b0d5893ed4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDataObject, IDataObject interface [COM], IDataObject interface [COM],described, _ole_idataobject, com.idataobject, objidl/IDataObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IDataObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IDataObject interface


## -description


Enables data transfer and notification of changes in data. Data transfer methods specify the format of the transferred data along with the medium through which the data is to be transferred. Optionally, the data can be rendered for a specific target device. In addition to methods for retrieving and storing data, the <b>IDataObject</b> interface specifies methods for enumerating available formats and managing connections to advisory sinks for handling change notifications.

The term <i>data object</i> is used to mean any object that supports an implementation of the <b>IDataObject</b> interface. Implementations vary, depending on what the data object is required to do; in some data objects, the implementation of certain methods not supported by the object could simply be the return of E_NOTIMPL. For example, some data objects do not allow callers to send them data. Other data objects do not support advisory connections and change notifications. However, for those data objects that do support change notifications, OLE provides an object called a data advise holder. An interface pointer to this holder is available through a call to the helper function <a href="https://msdn.microsoft.com/a2114f2f-106a-4a26-ba94-1b40af90a0f3">CreateDataAdviseHolder</a>. A data object can have multiple connections, each with its own set of attributes. The OLE data advise holder simplifies the task of managing these connections and sending the appropriate notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataObject</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IDataObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">DAdvise</a>
</td>
<td align="left" width="63%">
Creates a connection between a data object and an advise sink so the advise sink can receive notifications of changes in the data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">DUnadvise</a>
</td>
<td align="left" width="63%">
Destroys a notification previously set up with the <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">DAdvise</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/319637fd-d9b5-4da0-ac92-4c52fa9f5231">EnumDAdvise</a>
</td>
<td align="left" width="63%">
Creates and returns a pointer to an object to enumerate the current advisory connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">EnumFormatEtc</a>
</td>
<td align="left" width="63%">
Creates an object to enumerate the formats supported by a data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a5009a0-8d92-483a-b055-8a97f326dccd">GetCanonicalFormatEtc</a>
</td>
<td align="left" width="63%">
Provides a potentially different but logically equivalent <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
</td>
<td align="left" width="63%">
Called by a data consumer to obtain data from a source data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/802fc49a-21c2-4490-9b00-1359ce9c325f">GetDataHere</a>
</td>
<td align="left" width="63%">
Called by a data consumer to obtain data from a source data object. This method differs from the GetData method in that the caller must allocate and free the specified storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38a1bb4f-7762-4e74-a386-4ae05e59d15f">QueryGetData</a>
</td>
<td align="left" width="63%">
Determines whether the data object is capable of rendering the data as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">SetData</a>
</td>
<td align="left" width="63%">
Called by an object containing a data source to transfer data to the object that implements this method.

</td>
</tr>
</table> 

