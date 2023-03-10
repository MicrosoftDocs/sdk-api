---
UID: NF:vds.IVdsDisk3.GetProperties2
title: IVdsDisk3::GetProperties2 (vds.h)
description: Returns property information for a disk. This method is identical to the IVdsDisk::GetProperties method, except that it returns a VDS_DISK_PROP2 structure instead of a VDS_DISK_PROP structure.
helpviewer_keywords: ["GetProperties2","GetProperties2 method","GetProperties2 method","IVdsDisk3 interface","IVdsDisk3 interface","GetProperties2 method","IVdsDisk3.GetProperties2","IVdsDisk3::GetProperties2","base.ivdsdisk3_getproperties2","vds/IVdsDisk3::GetProperties2"]
old-location: base\ivdsdisk3_getproperties2.htm
tech.root: base
ms.assetid: ef88b61b-9139-4767-b54f-46122650e922
ms.date: 12/05/2018
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsDisk3 interface, IVdsDisk3 interface,GetProperties2 method, IVdsDisk3.GetProperties2, IVdsDisk3::GetProperties2, base.ivdsdisk3_getproperties2, vds/IVdsDisk3::GetProperties2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsDisk3::GetProperties2
 - vds/IVdsDisk3::GetProperties2
dev_langs:
 - c++
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
---

# IVdsDisk3::GetProperties2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns property 
   information for a disk. This method is identical to the <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a> method, except that it returns a <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a> structure instead of a <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> structure.

## -parameters

### -param pDiskProperties [out]

The address of the <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a> structure 
      allocated and passed in by the caller. VDS allocates memory for the <b>pwszDiskAddress</b>, 
      <b>pwszName</b>, <b>pwszFriendlyName</b>, 
      <b>pwszAdaptorName</b>, <b>pwszDevicePath</b>, and <b>pwszLocationPath</b> member strings. 
      Callers must free the strings by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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

In the <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a> structure that is returned in the <i>pDiskProperties</i> parameter, the <b>pwszDiskAddress</b> member   is optional and can be <b>NULL</b> if no value is available. Callers of this method must check whether this member is <b>NULL</b>.

For Hyper-V, the  <b>pwszLocationPath</b> member is <b>NULL</b>, because the virtual controller does not return the location path.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk3">IVdsDisk3</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>