---
UID: NF:objbase.CreateDataCache
title: CreateDataCache function
author: windows-sdk-content
description: Retrieves a pointer to a new instance of an OLE-provided implementation of a data cache.
old-location: com\createdatacache.htm
tech.root: com
ms.assetid: 8a64675b-1337-4555-b9a6-e19f9b987ba2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateDataCache, CreateDataCache function [COM], _ole_CreateDataCache, com.createdatacache, objbase/CreateDataCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
api_name:
 - CreateDataCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDataCache function


## -description


Retrieves a pointer to a new instance of an OLE-provided implementation of a data cache.




## -parameters




### -param pUnkOuter [in]

 If the cache is to be created as part of an aggregate, pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the aggregate. If not, the parameter should be <b>NULL</b>.


### -param rclsid [in]

CLSID used to generate icon labels. This value is typically CLSID_NULL.


### -param iid [in]

Reference to the identifier of the interface the caller wants to use to communicate with the cache. This value is typically IID_IOleCache (defined in the OLE headers to equal the interface identifier for <a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>).


### -param ppv [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer to the supplied cache object.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface represented by riid is not supported by the object. The parameter <i>ppvObj</i> is set to <b>NULL</b>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



The cache object created by <b>CreateDataCache</b> supports the <a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>, <a href="https://msdn.microsoft.com/8bbeca2d-c805-4116-b918-e2ddded8b160">IOleCache2</a>, and <a href="https://msdn.microsoft.com/64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a">IOleCacheControl</a> interfaces for controlling the cache. It also supports the <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> (without advise sinks), <a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>, and <a href="https://msdn.microsoft.com/b150ca4b-c53c-4bcb-85fa-461f9fa8b63b">IViewObject2</a> interfaces. 





## -see-also




<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/8bbeca2d-c805-4116-b918-e2ddded8b160">IOleCache2</a>



<a href="https://msdn.microsoft.com/64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a">IOleCacheControl</a>
 

 

