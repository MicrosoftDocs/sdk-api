---
UID: NN:objidl.IPersistStream
title: IPersistStream (objidl.h)
description: Enables the saving and loading of objects that use a simple serial stream for their storage needs.
helpviewer_keywords: ["IPersistStream","IPersistStream interface [COM]","IPersistStream interface [COM]","described","_com_ipersiststream","com.ipersiststream","objidl/IPersistStream"]
old-location: com\ipersiststream.htm
tech.root: com
ms.assetid: 97ea64ee-d950-4872-add6-1f532a6eb33f
ms.date: 12/05/2018
ms.keywords: IPersistStream, IPersistStream interface [COM], IPersistStream interface [COM],described, _com_ipersiststream, com.ipersiststream, objidl/IPersistStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistStream
 - objidl/IPersistStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistStream
---

# IPersistStream interface


## -description

Enables the saving and loading of objects that use a simple serial stream for their storage needs.

## -inheritance

The <b>IPersistStream</b> interface inherits from <b>IPersist</b>. <b>IPersistStream</b> also has these types of members:

## -remarks

One way in which this interface is used is to support OLE moniker implementations. Each of the OLE-provided moniker interfaces provides an <b>IPersistStream</b> implementation through which the moniker saves or loads itself. An instance of the OLE generic composite moniker class calls the <b>IPersistStream</b> methods of its component monikers to load or save the components in the proper sequence in a single stream.

<h3><a id="IPersistStream_URL_Moniker_Implementation"></a><a id="ipersiststream_url_moniker_implementation"></a><a id="IPERSISTSTREAM_URL_MONIKER_IMPLEMENTATION"></a>IPersistStream URL Moniker Implementation</h3>
The URL moniker implementation of <b>IPersistStream</b> is found on an URL moniker object, which supports <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, <b>IAsyncMoniker</b>, and <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>. The <b>IMoniker</b> interface inherits its definition from <b>IPersistStream</b> and thus, the URL moniker also provides an implementation of <b>IPersistStream</b> as part of its implementation of <b>IMoniker</b>.

The <a href="/previous-versions/ms775081(v=vs.85)">IAsyncMoniker</a> interface on an URL moniker is simply <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> (there are no additional methods); it is used to allow clients to determine if a moniker supports asynchronous binding. To get a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on this object, call the <b>CreateURLMonikerEx</b> function. Then, to get a pointer to <b>IPersistStream</b>, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method.

<b>IPersistStream</b>, in addition to inheriting its definition from <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, also inherits the single method of <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>, <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">GetClassID</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>
