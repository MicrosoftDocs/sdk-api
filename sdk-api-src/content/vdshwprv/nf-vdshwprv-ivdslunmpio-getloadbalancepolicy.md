---
UID: NF:vdshwprv.IVdsLunMpio.GetLoadBalancePolicy
title: IVdsLunMpio::GetLoadBalancePolicy
author: windows-sdk-content
description: Returns the current load balance policy on the LUN.
old-location: base\ivdslunmpio_getloadbalancepolicy.htm
tech.root: VDS
ms.assetid: 56866ecb-c84b-4297-9bd4-54969501bf9e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetLoadBalancePolicy, GetLoadBalancePolicy method [VDS], GetLoadBalancePolicy method [VDS],IVdsLunMpio interface, IVdsLunMpio interface [VDS],GetLoadBalancePolicy method, IVdsLunMpio.GetLoadBalancePolicy, IVdsLunMpio::GetLoadBalancePolicy, base.ivdslunmpio_getloadbalancepolicy, vds/IVdsLunMpio::GetLoadBalancePolicy, vdshwprv/IVdsLunMpio::GetLoadBalancePolicy
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsLunMpio.GetLoadBalancePolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsLunMpio::GetLoadBalancePolicy


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the current load balance policy on the LUN.


## -parameters




### -param pPolicy [out]

A pointer to a variable that receives an <a href="https://msdn.microsoft.com/0391c605-3808-4c24-8638-77b1fe3342bf">VDS_LOADBALANCE_POLICY_ENUM</a> enumeration value that specifies the load balance policy.


### -param ppPaths [out]

A pointer to the array of <a href="https://msdn.microsoft.com/7dec1d91-6781-42fa-9476-bb64e2554017">VDS_PATH_POLICY</a> structures passed in by the caller. Callers must free this array by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param plNumberOfPaths [out]

A pointer to a variable that receives the number of path-specific policy information structures returned in the 
      <i>ppPaths</i> parameter.
     


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The load balance policy was successfully returned. If the LUN has no paths, the array is empty, the value 
        pointed to by the  <i>plNumberOfPaths</i> parameter is set to 0, and the value pointed to 
        by the <i>ppPaths</i> parameter is set to <b>NULL</b>.

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
        method to  restore the cache.

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



The number of paths returned by this method will match the number of paths returned by 
    the <a href="https://msdn.microsoft.com/c7cc1abf-c7f2-4260-b9d2-f70128276e1e">IVdsLunMpio::GetPathInfo</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0c7ab50a-306e-44f8-976d-0e65e36b0fea">IVdsLunMpio</a>



<a href="https://msdn.microsoft.com/56866ecb-c84b-4297-9bd4-54969501bf9e">IVdsLunMpio::GetLoadBalancePolicy</a>



<a href="https://msdn.microsoft.com/0391c605-3808-4c24-8638-77b1fe3342bf">VDS_LOADBALANCE_POLICY_ENUM</a>



<a href="https://msdn.microsoft.com/7dec1d91-6781-42fa-9476-bb64e2554017">VDS_PATH_POLICY</a>
 

 

