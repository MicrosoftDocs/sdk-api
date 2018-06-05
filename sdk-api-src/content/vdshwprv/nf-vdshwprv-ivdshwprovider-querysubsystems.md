---
UID: NF:vdshwprv.IVdsHwProvider.QuerySubSystems
title: IVdsHwProvider::QuerySubSystems
author: windows-sdk-content
description: Returns an enumeration of the subsystems managed by the provider.
old-location: base\ivdshwprovider_querysubsystems.htm
old-project: VDS
ms.assetid: ae327655-3db9-44b0-934a-458ee90b1d07
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsHwProvider interface [VDS],QuerySubSystems method, IVdsHwProvider.QuerySubSystems, IVdsHwProvider::QuerySubSystems, QuerySubSystems, QuerySubSystems method [VDS], QuerySubSystems method [VDS],IVdsHwProvider interface, base.ivdshwprovider_querysubsystems, vds/IVdsHwProvider::QuerySubSystems, vdshwprv/IVdsHwProvider::QuerySubSystems
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsHwProvider.QuerySubSystems
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsHwProvider::QuerySubSystems


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns 
   an enumeration of the subsystems managed by the provider.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the subsystems  as <a href="https://msdn.microsoft.com/f605a5de-9256-4b43-8e12-3d78fd6cd9f1">subsystem objects</a>. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the subsystem objects when they are no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Returns the enumeration of subsystem identifiers. If the provider manages no subsystems, the enumeration 
        is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
        <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> method to restore 
        the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The provider is in a failed state, and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or 
        operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZE_NOT_CALLED</b></dt>
<dt>0x80042402L</dt>
</dl>
</td>
<td width="60%">
The initialization method has not been called.

</td>
</tr>
</table>
 




## -remarks



The returned object enumerates all subsystems currently connected to the network. Use the 
   <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method to 
    discover new subsystems. Use the 
    <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>method to refresh the 
    internally-cached provider data for existing subsystems.




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>



<a href="https://msdn.microsoft.com/ff90875d-f437-4236-a13f-d55a83b778b9">IVdsHwProvider</a>



<a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>
 

 

