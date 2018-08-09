---
UID: NF:vdshwprv.IVdsLunMpio.GetSupportedLbPolicies
title: IVdsLunMpio::GetSupportedLbPolicies
author: windows-sdk-content
description: Retrieves the load balance policies that are supported by the hardware provider.
old-location: base\ivdslunmpio_getsupportedlbpolicies.htm
old-project: vds
ms.assetid: 1b1f3437-41db-403e-abdb-febbfe90858c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSupportedLbPolicies, GetSupportedLbPolicies method [VDS], GetSupportedLbPolicies method [VDS],IVdsLunMpio interface, IVdsLunMpio interface [VDS],GetSupportedLbPolicies method, IVdsLunMpio.GetSupportedLbPolicies, IVdsLunMpio::GetSupportedLbPolicies, base.ivdslunmpio_getsupportedlbpolicies, vds/IVdsLunMpio::GetSupportedLbPolicies, vdshwprv/IVdsLunMpio::GetSupportedLbPolicies
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
 - IVdsLunMpio.GetSupportedLbPolicies
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLunMpio::GetSupportedLbPolicies


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Retrieves the load balance policies that are supported by the hardware provider.


## -parameters




### -param pulLbFlags [out]

The address of a <b>ULONG</b> that will receive the supported flags (as enumerated by 
      the <a href="https://msdn.microsoft.com/bfc9aabf-b9ce-4b36-b68a-b74628092962">VDS_PROVIDER_LBSUPPORT_FLAG</a> enumeration.)


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The load balance policy was successfully returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0c7ab50a-306e-44f8-976d-0e65e36b0fea">IVdsLunMpio</a>



<a href="https://msdn.microsoft.com/bfc9aabf-b9ce-4b36-b68a-b74628092962">VDS_PROVIDER_LBSUPPORT_FLAG</a>
 

 

