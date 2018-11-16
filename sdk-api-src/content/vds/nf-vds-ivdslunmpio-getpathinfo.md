---
UID: NF:vds.IVdsLunMpio.GetPathInfo
title: IVdsLunMpio::GetPathInfo
author: windows-sdk-content
description: Returns an array of VDS_PATH_INFO structures, one for each path to the LUN.
old-location: base\ivdslunmpio_getpathinfo.htm
tech.root: VDS
ms.assetid: c7cc1abf-c7f2-4260-b9d2-f70128276e1e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetPathInfo, GetPathInfo method [VDS], GetPathInfo method [VDS],IVdsLunMpio interface, IVdsLunMpio interface [VDS],GetPathInfo method, IVdsLunMpio.GetPathInfo, IVdsLunMpio::GetPathInfo, base.ivdslunmpio_getpathinfo, vds/IVdsLunMpio::GetPathInfo, vdshwprv/IVdsLunMpio::GetPathInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
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
 - IVdsLunMpio.GetPathInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
- apiref
: 
- COM
: 
- vds.h
: 
- IVdsLunMpio.GetPathInfo
: 
---

# IVdsLunMpio::GetPathInfo


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an array of <a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a> structures, 
     one for each path to the LUN.


## -parameters




### -param ppPaths [out]

The address of a variable that receives an array of <a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a> structures. Callers must free each element in the array, and the array itself, by using 
      the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param plNumberOfPaths [out]

The address of a variable that receives the number of elements in the array returned in the 
      <i>ppPaths</i> parameter.
      

The number of paths returned by this method will match the number of paths returned by the 
       <a href="https://msdn.microsoft.com/56866ecb-c84b-4297-9bd4-54969501bf9e">IVdsLunMpio::GetLoadBalancePolicy</a> 
       method.


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
The path information was successfully returned.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> 
        method to restore the cache.

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
Another operation is in progress. This operation cannot proceed until previous operations are 
        complete.

</td>
</tr>
</table>
 




## -remarks



Hardware providers do not need to return the <b>VDS_OBJECT_ID</b> at hbaPortProp.id of 
    <a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a> and should just set this to 
    <b>GUID_NULL</b>. This ID will be filled in by the system when this call is passed back to 
    applications. If the service cannot find the corresponding HBA port,  <b>GUID_NULL</b> will be 
    used. The application will interpret this to mean that the HBA port is unknown to VDS.




## -see-also




<a href="https://msdn.microsoft.com/0c7ab50a-306e-44f8-976d-0e65e36b0fea">IVdsLunMpio</a>



<a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a>
 

 

