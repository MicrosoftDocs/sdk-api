---
UID: NF:vds.IVdsVolume2.GetProperties2
title: IVdsVolume2::GetProperties2
author: windows-sdk-content
description: Returns property information for the current volume. This method is identical to the IVdsVolume::GetProperties method, except that it returns a VDS_VOLUME_PROP2 structure instead of a VDS_VOLUME_PROP structure.
old-location: base\ivdsvolume2_getproperties2.htm
tech.root: vds
ms.assetid: 9580ceb2-6b2f-4313-a140-f6fa6a366960
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsVolume2 interface, IVdsVolume2 interface,GetProperties2 method, IVdsVolume2.GetProperties2, IVdsVolume2::GetProperties2, base.ivdsvolume2_getproperties2, vds/IVdsVolume2::GetProperties2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsVolume2.GetProperties2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolume2::GetProperties2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns 
   property information for the current volume. This method is identical to the <a href="https://msdn.microsoft.com/ba4a92c9-35f1-463a-8fa3-1a0d78720555">IVdsVolume::GetProperties</a> method, except that it returns a <a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a> structure instead of a <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a> structure.


## -parameters




### -param pVolumeProperties [out]

The address of the <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP2</a> structure 
      allocated and passed in by the caller. VDS allocates memory for the <b>pwszName</b> member 
      string. Callers must free the string by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


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
The method completed successfully.

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
</table>
 




## -remarks



This method retrieves the unique volume identifier for a volume. The structure that contains that identifier is <a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a>, not <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>.

Note that a unique volume identifier is not the same as a volume GUID path. To find the volume GUID paths for a volume, use the <a href="https://msdn.microsoft.com/08311403-23a9-4191-9720-3cec805de825">IVdsVolumeMF3::QueryVolumeGuidPathnames</a> method.




## -see-also




<a href="https://msdn.microsoft.com/78077ce6-04f7-4d76-9057-40941feb941b">IVdsVolume2</a>
 

 

