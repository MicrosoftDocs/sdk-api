---
UID: NF:vds.IVdsIscsiInitiatorPortal.GetInitiatorAdapter
title: IVdsIscsiInitiatorPortal::GetInitiatorAdapter
author: windows-sdk-content
description: Returns the initiator adapter to which the initiator portal belongs.
old-location: base\ivdsiscsiinitiatorportal_getinitiatoradapter.htm
tech.root: vds
ms.assetid: fcdd2083-36e0-4924-9af0-87a9fe4711e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInitiatorAdapter, GetInitiatorAdapter method [VDS], GetInitiatorAdapter method [VDS],IVdsIscsiInitiatorPortal interface, IVdsIscsiInitiatorPortal interface [VDS],GetInitiatorAdapter method, IVdsIscsiInitiatorPortal.GetInitiatorAdapter, IVdsIscsiInitiatorPortal::GetInitiatorAdapter, base.ivdsiscsiinitiatorportal_getinitiatoradapter, vds/IVdsIscsiInitiatorPortal::GetInitiatorAdapter
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
 - IVdsIscsiInitiatorPortal.GetInitiatorAdapter
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiInitiatorPortal::GetInitiatorAdapter


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the initiator adapter to which the initiator portal belongs.


## -parameters




### -param ppInitiatorAdapter [out]

The address of an <a href="https://msdn.microsoft.com/3f911878-28c6-41db-ae9c-81e282aabf9d">IVdsIscsiInitiatorAdapter</a> 
      interface pointer. VDS initializes the interface on return. Callers must release the interface.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The initiator adapter was returned successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3f911878-28c6-41db-ae9c-81e282aabf9d">IVdsIscsiInitiatorAdapter</a>



<a href="https://msdn.microsoft.com/ae64cc73-4f36-4846-a1c0-f329de6299ee">IVdsIscsiInitiatorPortal</a>
 

 

