---
UID: NF:vds.IVdsLunMpio.SetLoadBalancePolicy
title: IVdsLunMpio::SetLoadBalancePolicy
author: windows-sdk-content
description: Sets the load balance policy on the LUN.
old-location: base\ivdslunmpio_setloadbalancepolicy.htm
old-project: VDS
ms.assetid: 2f3eb00a-864e-4fb7-a722-4537e6b8dd42
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsLunMpio interface [VDS],SetLoadBalancePolicy method, IVdsLunMpio.SetLoadBalancePolicy, IVdsLunMpio::SetLoadBalancePolicy, SetLoadBalancePolicy, SetLoadBalancePolicy method [VDS], SetLoadBalancePolicy method [VDS],IVdsLunMpio interface, base.ivdslunmpio_setloadbalancepolicy, vds/IVdsLunMpio::SetLoadBalancePolicy, vdshwprv/IVdsLunMpio::SetLoadBalancePolicy
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	IVdsLunMpio.SetLoadBalancePolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLunMpio::SetLoadBalancePolicy


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Sets the load balance policy on the LUN.


## -parameters




### -param policy


      The load balance policy enumerated by the  
      <a href="https://msdn.microsoft.com/0391c605-3808-4c24-8638-77b1fe3342bf">VDS_LOADBALANCE_POLICY_ENUM</a> enumeration.


### -param pPaths

A 
      pointer to an array of members of the <a href="https://msdn.microsoft.com/7dec1d91-6781-42fa-9476-bb64e2554017">VDS_PATH_POLICY</a> structure 
      that contain the path-specific policy information.


### -param lNumberOfPaths


      The number of members of the <a href="https://msdn.microsoft.com/7dec1d91-6781-42fa-9476-bb64e2554017">VDS_PATH_POLICY</a> structure in the array 
      pointed to by the <i>pPaths</i> parameter.


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

        The load balance policy was successfully set.

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




<a href="https://msdn.microsoft.com/0c7ab50a-306e-44f8-976d-0e65e36b0fea">IVdsLunMpio</a>



<a href="https://msdn.microsoft.com/56866ecb-c84b-4297-9bd4-54969501bf9e">IVdsLunMpio::GetLoadBalancePolicy</a>



<a href="https://msdn.microsoft.com/0391c605-3808-4c24-8638-77b1fe3342bf">VDS_LOADBALANCE_POLICY_ENUM</a>



<a href="https://msdn.microsoft.com/7dec1d91-6781-42fa-9476-bb64e2554017">VDS_PATH_POLICY</a>
 

 

