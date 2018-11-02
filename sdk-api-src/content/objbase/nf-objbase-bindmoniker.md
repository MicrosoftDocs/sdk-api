---
UID: NF:objbase.BindMoniker
title: BindMoniker function
author: windows-sdk-content
description: Locates an object by means of its moniker, activates the object if it is inactive, and retrieves a pointer to the specified interface on that object.
old-location: com\bindmoniker.htm
tech.root: com
ms.assetid: 5a022c39-fc2c-458b-9dfe-fed1255d49a4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: BindMoniker, BindMoniker function [COM], _com_BindMoniker, com.bindmoniker, objbase/BindMoniker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - BindMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BindMoniker function


## -description


Locates an object by means of its moniker, activates the object if it is inactive, and retrieves a pointer to the specified interface on that object.


## -parameters




### -param pmk [in]

A pointer to the object's moniker. See <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>.


### -param grfOpt [in]

This parameter is reserved for future use and must be 0.


### -param iidResult [in]

The interface identifier to be used to communicate with the object.


### -param ppvResult [out]

The address of pointer variable that receives the interface pointer requested in <i>iidResult</i>. Upon successful return, *<i>ppvResult</i> contains the requested interface pointer. If an error occurs, *<i>ppvResult</i> is <b>NULL</b>. If the call is successful, the caller is responsible for releasing the pointer with a call to the object's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method.


## -returns



This function can return the following error codes, or any of the error values returned by the <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> method.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The object was located and activated, if necessary, and a pointer to the requested interface was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object that the moniker object identified could not be found.

</td>
</tr>
</table>
 




## -remarks



<b>BindMoniker</b> is a helper function supplied as a convenient way for a client that has the moniker of an object to obtain a pointer to one of that object's interfaces. <b>BindMoniker</b> packages the following calls:

<pre class="syntax" xml:space="preserve"><code>CreateBindCtx(0, &amp;pbc); 
pmk-&gt;BindToObject(pbc, NULL, riid, ppvObj);</code></pre>

<a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> creates a bind context object that supports the system implementation of IBindContext. The pmk parameter is actually a pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> implementation on a moniker object. This implementation's <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">BindToObject</a> method supplies the pointer to the requested interface pointer.

If you have several monikers to bind in quick succession and if you know that those monikers will activate the same object, it may be more efficient to call the <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> method directly, which enables you to use the same bind context object for all the monikers. See the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface for more information.

Container applications that allow their documents to contain linked objects are a special client that generally does not make direct calls to <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> methods. Instead, the client manipulates the linked objects through the <a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a> interface. The default handler implements this interface and calls the appropriate <b>IMoniker</b> methods as needed. 





## -see-also




<a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a>



<a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a>
 

 

