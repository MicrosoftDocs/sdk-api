---
UID: NF:vds.IVdsIscsiInitiatorAdapter.QueryInitiatorPortals
title: IVdsIscsiInitiatorAdapter::QueryInitiatorPortals (vds.h)
author: windows-sdk-content
description: Returns an object that enumerates the iSCSI initiator portals of the initiator adapter.
old-location: base\ivdsiscsiinitiatoradapter_queryinitiatorportals.htm
tech.root: VDS
ms.assetid: d3c893c0-167f-46f5-92f8-aa61f5e16542
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsIscsiInitiatorAdapter interface [VDS],QueryInitiatorPortals method, IVdsIscsiInitiatorAdapter.QueryInitiatorPortals, IVdsIscsiInitiatorAdapter::QueryInitiatorPortals, QueryInitiatorPortals, QueryInitiatorPortals method [VDS], QueryInitiatorPortals method [VDS],IVdsIscsiInitiatorAdapter interface, base.ivdsiscsiinitiatoradapter_queryinitiatorportals, vds/IVdsIscsiInitiatorAdapter::QueryInitiatorPortals
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
 - IVdsIscsiInitiatorAdapter.QueryInitiatorPortals
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiInitiatorAdapter::QueryInitiatorPortals


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an object that enumerates the iSCSI initiator portals of  the initiator adapter.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface pointer that can be used to enumerate the  initiator portals  as <a href="https://msdn.microsoft.com/ae4d18f2-4d50-480c-bc7a-4eec0334707d">initiator portal objects</a>. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the initiator portal objects when they are no longer needed by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.
     


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
The enumeration of initiator portals was successfully returned. If the initiator adapter has no portals, the 
        enumeration is empty.
       

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>



<a href="https://msdn.microsoft.com/3f911878-28c6-41db-ae9c-81e282aabf9d">IVdsIscsiInitiatorAdapter</a>
 

 

