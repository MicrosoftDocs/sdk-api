---
UID: NF:vds.IVdsDisk.GetIdentificationData
title: IVdsDisk::GetIdentificationData (vds.h)
author: windows-sdk-content
description: Retrieves information that uniquely identifies a disk.
old-location: base\ivdsdisk_getidentificationdata.htm
tech.root: VDS
ms.assetid: 400fa102-f98a-4bc1-919c-858c135a5b93
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIdentificationData, GetIdentificationData method [VDS], GetIdentificationData method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],GetIdentificationData method, IVdsDisk.GetIdentificationData, IVdsDisk::GetIdentificationData, base.ivdsdisk_getidentificationdata, vds/IVdsDisk::GetIdentificationData
ms.topic: method
req.header: vds.h
req.include-header: 
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
 - IVdsDisk.GetIdentificationData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsDisk::GetIdentificationData


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Retrieves information that uniquely identifies a disk.


## -parameters




### -param pLunInfo [out]

The address of the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>structure allocated and passed in by the caller. VDS allocates memory for the <b>m_szVendorId</b>, 
      <b>m_szProductId</b>, <b>m_szProductRevision</b>, 
      and <b>m_szSerialNumber</b> member strings, as well as the <b>m_pbPort</b> and   <b>m_pbAddress</b> member strings of each element in the array of <a href="https://msdn.microsoft.com/fc9f532b-a37f-4338-95db-6ec988131211">VDS_INTERCONNECT</a> structures. 
      Callers must free the strings by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The identification data was returned successfully.

</td>
</tr>
</table>
 




## -remarks



VDS implements this method. Callers can only extract LUN information from devices managed by a hardware provider.




## -see-also




<a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a>



<a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>
 

 

