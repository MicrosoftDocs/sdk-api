---
UID: NF:vds.IVdsDisk3.GetProperties2
title: IVdsDisk3::GetProperties2
author: windows-sdk-content
description: Returns property information for a disk. This method is identical to the IVdsDisk::GetProperties method, except that it returns a VDS_DISK_PROP2 structure instead of a VDS_DISK_PROP structure.
old-location: base\ivdsdisk3_getproperties2.htm
old-project: vds
ms.assetid: ef88b61b-9139-4767-b54f-46122650e922
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsDisk3 interface, IVdsDisk3 interface,GetProperties2 method, IVdsDisk3.GetProperties2, IVdsDisk3::GetProperties2, base.ivdsdisk3_getproperties2, vds/IVdsDisk3::GetProperties2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.redist: 
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
 - IVdsDisk3.GetProperties2
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDisk3::GetProperties2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns property 
   information for a disk. This method is identical to the <a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a> method, except that it returns a <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structure instead of a <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> structure.


## -parameters




### -param pDiskProperties [out]

The address of the <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structure 
      allocated and passed in by the caller. VDS allocates memory for the <b>pwszDiskAddress</b>, 
      <b>pwszName</b>, <b>pwszFriendlyName</b>, 
      <b>pwszAdaptorName</b>, <b>pwszDevicePath</b>, and <b>pwszLocationPath</b> member strings. 
      Callers must free the strings by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The properties were returned successfully.

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



In the <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structure that is returned in the <i>pDiskProperties</i> parameter, the <b>pwszDiskAddress</b> member   is optional and can be <b>NULL</b> if no value is available. Callers of this method must check whether this member is <b>NULL</b>.

For Hyper-V, the  <b>pwszLocationPath</b> member is <b>NULL</b>, because the virtual controller does not return the location path.




## -see-also




<a href="https://msdn.microsoft.com/e3004195-b180-4053-bf91-8f1a0e72f5a6">IVdsDisk3</a>



<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>
 

 

