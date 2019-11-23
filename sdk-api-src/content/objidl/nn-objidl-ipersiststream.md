---
UID: NN:objidl.IPersistStream
title: IPersistStream (objidl.h)

description: Enables the saving and loading of objects that use a simple serial stream for their storage needs.
old-location: com\ipersiststream.htm
tech.root: com
ms.assetid: 97ea64ee-d950-4872-add6-1f532a6eb33f

ms.date: 12/05/2018
ms.keywords: IPersistStream, IPersistStream interface [COM], IPersistStream interface [COM],described, _com_ipersiststream, com.ipersiststream, objidl/IPersistStream
ms.topic: interface
f1_keywords: 
 - "objidl/IPersistStream"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistStream interface


## -description


Enables the saving and loading of objects that use a simple serial stream for their storage needs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistStream</b> interface inherits from <b>IPersist</b>. <b>IPersistStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststream-getsizemax">GetSizeMax</a>
</td>
<td align="left" width="63%">
Retrieves the size of the stream needed to save the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststream-isdirty">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststream-load">Load</a>
</td>
<td align="left" width="63%">
Initializes an object from the stream where it was saved previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststream-save">Save</a>
</td>
<td align="left" width="63%">
Saves an object to the specified stream.

</td>
</tr>
</table> 


## -remarks



One way in which this interface is used is to support OLE moniker implementations. Each of the OLE-provided moniker interfaces provides an <b>IPersistStream</b> implementation through which the moniker saves or loads itself. An instance of the OLE generic composite moniker class calls the <b>IPersistStream</b> methods of its component monikers to load or save the components in the proper sequence in a single stream.

<h3><a id="IPersistStream_URL_Moniker_Implementation"></a><a id="ipersiststream_url_moniker_implementation"></a><a id="IPERSISTSTREAM_URL_MONIKER_IMPLEMENTATION"></a>IPersistStream URL Moniker Implementation</h3>
The URL moniker implementation of <b>IPersistStream</b> is found on an URL moniker object, which supports <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, <b>IAsyncMoniker</b>, and <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>. The <b>IMoniker</b> interface inherits its definition from <b>IPersistStream</b> and thus, the URL moniker also provides an implementation of <b>IPersistStream</b> as part of its implementation of <b>IMoniker</b>.

The <a href="https://docs.microsoft.com/previous-versions/ms775081(v=vs.85)">IAsyncMoniker</a> interface on an URL moniker is simply <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> (there are no additional methods); it is used to allow clients to determine if a moniker supports asynchronous binding. To get a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on this object, call the <b>CreateURLMonikerEx</b> function. Then, to get a pointer to <b>IPersistStream</b>, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method.

<b>IPersistStream</b>, in addition to inheriting its definition from <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, also inherits the single method of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">GetClassID</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>
 

 

