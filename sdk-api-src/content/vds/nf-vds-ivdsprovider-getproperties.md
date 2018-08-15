---
UID: NF:vds.IVdsProvider.GetProperties
title: IVdsProvider::GetProperties
author: windows-sdk-content
description: Returns the properties of a provider.
old-location: base\ivdsprovider_getproperties.htm
old-project: vds
ms.assetid: a4cb18c5-2cda-4d0a-9be0-4a548ec2f6eb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsProvider interface, IVdsProvider interface [VDS],GetProperties method, IVdsProvider.GetProperties, IVdsProvider::GetProperties, base.ivdsprovider_getproperties, vds/IVdsProvider::GetProperties, vdshwprv/IVdsProvider::GetProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.redist: 
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsProvider.GetProperties
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsProvider::GetProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the 
   properties of a provider.


## -parameters




### -param pProviderProp [out]

The address of the <a href="https://msdn.microsoft.com/f41fc908-3720-4dfb-a5d3-bb1459fb7e5d">VDS_PROVIDER_PROP</a> 
      structure allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszName</b> and <b>pwszVersion</b> member strings. Callers must free 
      the strings by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>function.


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
<dt><b><b>VDS_S_PROPERTIES_INCOMPLETE</b></b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c09aa32f-d859-44b1-8656-973ba1b6a167">IVdsProvider</a>



<a href="https://msdn.microsoft.com/f41fc908-3720-4dfb-a5d3-bb1459fb7e5d">VDS_PROVIDER_PROP</a>
 

 

