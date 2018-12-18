---
UID: NF:vdshwprv.IVdsProviderPrivate.GetObject
title: IVdsProviderPrivate::GetObject
author: windows-sdk-content
description: Returns the specified object.
old-location: base\ivdsproviderprivate_getobject.htm
tech.root: vds
ms.assetid: 3f346255-c5c6-4ca3-9718-0347c3f8294a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetObject, GetObject method [VDS], GetObject method [VDS],IVdsProviderPrivate interface, IVdsProviderPrivate interface [VDS],GetObject method, IVdsProviderPrivate.GetObject, IVdsProviderPrivate::GetObject, base.ivdsproviderprivate_getobject, vdshwprv/IVdsProviderPrivate::GetObject
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsProviderPrivate.GetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsProviderPrivate::GetObject


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the specified object. 


## -parameters




### -param ObjectId [in]

The GUID of the object.


### -param type [in]

The object type enumerated by <a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a>.


### -param ppObjectUnk [out]

The address of an <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer for the object. When the pointer is no longer needed, the caller should release it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method. 


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The object was not found.

</td>
</tr>
</table>
 




## -remarks



The object can be a  subsystem, controller, LUN, LUN plex, drive, pack, disk, volume, or volume plex object. Each object represents a physical device (such as a subsystem, drive, or controllers) or a virtual device (such as a LUN or LUN plex). The hardware provider should create one COM object for each physical or virtual device.




## -see-also




<a href="https://msdn.microsoft.com/5f1c38bf-85a7-4123-becb-e8abf3052b41">IVdsProviderPrivate</a>



<a href="https://msdn.microsoft.com/63997e08-b6d3-4011-8946-56ef9832c0e4">VDS_OBJECT_TYPE</a>
 

 

