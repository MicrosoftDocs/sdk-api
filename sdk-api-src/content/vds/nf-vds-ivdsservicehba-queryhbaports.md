---
UID: NF:vds.IVdsServiceHba.QueryHbaPorts
title: IVdsServiceHba::QueryHbaPorts
author: windows-sdk-content
description: Returns an IEnumVdsObject enumeration object containing a list of the HBA ports known to VDS on the local system.
old-location: base\ivdsservicehba_queryhbaports.htm
tech.root: vds
ms.assetid: 2f81e5e9-5563-4435-8ecb-82f2c385c3dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsServiceHba interface [VDS],QueryHbaPorts method, IVdsServiceHba.QueryHbaPorts, IVdsServiceHba::QueryHbaPorts, QueryHbaPorts, QueryHbaPorts method [VDS], QueryHbaPorts method [VDS],IVdsServiceHba interface, base.ivdsservicehba_queryhbaports, vds/IVdsServiceHba::QueryHbaPorts
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
api_name:
 - IVdsServiceHba.QueryHbaPorts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsServiceHba::QueryHbaPorts


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> enumeration object containing 
     a list of the HBA ports known to VDS on the local system.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface pointer that can be used to enumerate the HBA ports  as <a href="https://msdn.microsoft.com/ae4d18f2-4d50-480c-bc7a-4eec0334707d">HBA port objects</a>. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the HBA port objects when they are no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


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
The enumeration of HBA ports was returned successfully. If the local system has no HBA ports, the enumeration 
        is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the VDS service finishes initializing, 
        the method is blocked until the initialization is complete. If the initialization fails, this error is returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>



<a href="https://msdn.microsoft.com/0f3375fa-fc17-4808-ac29-a772a9c13850">IVdsServiceHba</a>
 

 

