---
UID: NF:vdshwprv.IVdsLunControllerPorts.QueryActiveControllerPorts
title: IVdsLunControllerPorts::QueryActiveControllerPorts
author: windows-sdk-content
description: Returns an enumeration of currently active controller ports.
old-location: base\ivdsluncontrollerports_queryactivecontrollerports.htm
old-project: vds
ms.assetid: 0a6f34c6-f333-4abf-ad37-b7756b125045
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsLunControllerPorts interface,QueryActiveControllerPorts method, IVdsLunControllerPorts.QueryActiveControllerPorts, IVdsLunControllerPorts::QueryActiveControllerPorts, QueryActiveControllerPorts, QueryActiveControllerPorts method, QueryActiveControllerPorts method,IVdsLunControllerPorts interface, base.ivdsluncontrollerports_queryactivecontrollerports, vds/IVdsLunControllerPorts::QueryActiveControllerPorts, vdshwprv/IVdsLunControllerPorts::QueryActiveControllerPorts
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsLunControllerPorts.QueryActiveControllerPorts
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLunControllerPorts::QueryActiveControllerPorts


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an enumeration of currently active controller ports— 
    the controller ports through which the LUN can be accessed. This method replaces 
    <a href="https://msdn.microsoft.com/82561e4a-f2c2-46da-96bb-fbd50d4f7c39">IVdsLun::QueryActiveControllers</a>.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface pointer that can be used to enumerate the controller ports  as <a href="https://msdn.microsoft.com/5f94bcdc-93ab-4522-88bd-009a049b5dc9">controller port objects</a>. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the controller port objects when they are no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.
     


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The enumeration of controller ports was successfully returned. If the LUN has no active controller ports, the 
        enumeration is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> method to 
        restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_DELETED</b></b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The LUN object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_STATUS_FAILED</b></b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The LUN is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until previous operations are complete.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/82561e4a-f2c2-46da-96bb-fbd50d4f7c39">IVdsLun::QueryActiveControllers</a>



<a href="https://msdn.microsoft.com/81e48874-8bc2-4b82-bcf8-ce87f99ca3ad">IVdsLunControllerPorts</a>
 

 

