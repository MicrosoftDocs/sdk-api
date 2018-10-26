---
UID: NF:vds.IVdsHbaPort.GetProperties
title: IVdsHbaPort::GetProperties
author: windows-sdk-content
description: Retrieves the properties of an HBA port.
old-location: base\ivdshbaport_getproperties.htm
tech.root: VDS
ms.assetid: 5472534f-66c8-4a78-a351-92f59e50ae32
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsHbaPort interface, IVdsHbaPort interface [VDS],GetProperties method, IVdsHbaPort.GetProperties, IVdsHbaPort::GetProperties, base.ivdshbaport_getproperties, vds/IVdsHbaPort::GetProperties
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
 - IVdsHbaPort.GetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsHbaPort::GetProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Retrieves the properties of an HBA port.


## -parameters




### -param pHbaPortProp [out]

The address of a member of the <a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a> structure 
      that is allocated and passed in by the caller.


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
The properties were successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_S_PROPERTIES_INCOMPLETE</b></b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>pHbaPortProp</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/beb6ae5c-b70a-4dbc-b16f-1b398a569f15">IVdsHbaPort</a>



<a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a>
 

 

