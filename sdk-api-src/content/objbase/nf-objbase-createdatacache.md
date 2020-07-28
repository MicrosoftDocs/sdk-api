---
UID: NF:objbase.CreateDataCache
title: CreateDataCache function (objbase.h)
description: Retrieves a pointer to a new instance of an OLE-provided implementation of a data cache.
helpviewer_keywords: ["CreateDataCache","CreateDataCache function [COM]","_ole_CreateDataCache","com.createdatacache","objbase/CreateDataCache"]
old-location: com\createdatacache.htm
tech.root: com
ms.assetid: 8a64675b-1337-4555-b9a6-e19f9b987ba2
ms.date: 12/05/2018
ms.keywords: CreateDataCache, CreateDataCache function [COM], _ole_CreateDataCache, com.createdatacache, objbase/CreateDataCache
f1_keywords:
- objbase/CreateDataCache
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateDataCache function


## -description


Retrieves a pointer to a new instance of an OLE-provided implementation of a data cache.




## -parameters




### -param pUnkOuter [in]

 If the cache is to be created as part of an aggregate, pointer to the controlling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the aggregate. If not, the parameter should be <b>NULL</b>.


### -param rclsid [in]

CLSID used to generate icon labels. This value is typically CLSID_NULL.


### -param iid [in]

Reference to the identifier of the interface the caller wants to use to communicate with the cache. This value is typically IID_IOleCache (defined in the OLE headers to equal the interface identifier for <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>).


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



The cache object created by <b>CreateDataCache</b> supports the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>, <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache2">IOleCache2</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecachecontrol">IOleCacheControl</a> interfaces for controlling the cache. It also supports the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> (without advise sinks), <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject2">IViewObject2</a> interfaces. 





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache2">IOleCache2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecachecontrol">IOleCacheControl</a>
 

 

