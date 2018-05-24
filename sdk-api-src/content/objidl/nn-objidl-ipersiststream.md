---
UID: NN:objidl.IPersistStream
title: IPersistStream
author: windows-driver-content
description: Enables the saving and loading of objects that use a simple serial stream for their storage needs.
old-location: com\ipersiststream.htm
old-project: com
ms.assetid: 97ea64ee-d950-4872-add6-1f532a6eb33f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IPersistStream, IPersistStream interface [COM], IPersistStream interface [COM],described, _com_ipersiststream, com.ipersiststream, objidl/IPersistStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IPersistStream
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/ef9f0afe-b7e5-4b88-b59d-1371ffeaacb8">GetSizeMax</a>
</td>
<td align="left" width="63%">
Retrieves the size of the stream needed to save the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fabafc37-18f2-4def-b6bf-f7daa2bb8f37">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/351e1187-9959-4542-8778-925457c3b8e3">Load</a>
</td>
<td align="left" width="63%">
Initializes an object from the stream where it was saved previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
Saves an object to the specified stream.

</td>
</tr>
</table> 


## -remarks



One way in which this interface is used is to support OLE moniker implementations. Each of the OLE-provided moniker interfaces provides an <b>IPersistStream</b> implementation through which the moniker saves or loads itself. An instance of the OLE generic composite moniker class calls the <b>IPersistStream</b> methods of its component monikers to load or save the components in the proper sequence in a single stream.

<h3><a id="IPersistStream_URL_Moniker_Implementation"></a><a id="ipersiststream_url_moniker_implementation"></a><a id="IPERSISTSTREAM_URL_MONIKER_IMPLEMENTATION"></a>IPersistStream URL Moniker Implementation</h3>
The URL moniker implementation of <b>IPersistStream</b> is found on an URL moniker object, which supports <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, <b>IAsyncMoniker</b>, and <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>. The <b>IMoniker</b> interface inherits its definition from <b>IPersistStream</b> and thus, the URL moniker also provides an implementation of <b>IPersistStream</b> as part of its implementation of <b>IMoniker</b>.

The <a href="_inet_IAsyncMoniker_Interface_cpp">IAsyncMoniker</a> interface on an URL moniker is simply <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> (there are no additional methods); it is used to allow clients to determine if a moniker supports asynchronous binding. To get a pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on this object, call the <b>CreateURLMonikerEx</b> function. Then, to get a pointer to <b>IPersistStream</b>, call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method.

<b>IPersistStream</b>, in addition to inheriting its definition from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, also inherits the single method of <a href="https://msdn.microsoft.com/932eb0e2-35a6-482e-9138-00cff30508a9">IPersist</a>, <a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">GetClassID</a>.




## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a>
 

 

