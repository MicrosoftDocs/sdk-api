---
UID: NF:vds.IVdsVolume2.GetProperties2
title: IVdsVolume2::GetProperties2 (vds.h)
description: Returns property information for the current volume. This method is identical to the IVdsVolume::GetProperties method, except that it returns a VDS_VOLUME_PROP2 structure instead of a VDS_VOLUME_PROP structure.
helpviewer_keywords: ["GetProperties2","GetProperties2 method","GetProperties2 method","IVdsVolume2 interface","IVdsVolume2 interface","GetProperties2 method","IVdsVolume2.GetProperties2","IVdsVolume2::GetProperties2","base.ivdsvolume2_getproperties2","vds/IVdsVolume2::GetProperties2"]
old-location: base\ivdsvolume2_getproperties2.htm
tech.root: base
ms.assetid: 9580ceb2-6b2f-4313-a140-f6fa6a366960
ms.date: 12/05/2018
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsVolume2 interface, IVdsVolume2 interface,GetProperties2 method, IVdsVolume2.GetProperties2, IVdsVolume2::GetProperties2, base.ivdsvolume2_getproperties2, vds/IVdsVolume2::GetProperties2
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
 - IVdsVolume2::GetProperties2
 - vds/IVdsVolume2::GetProperties2
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
 - IVdsVolume2.GetProperties2
---

# IVdsVolume2::GetProperties2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns 
   property information for the current volume. This method is identical to the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-getproperties">IVdsVolume::GetProperties</a> method, except that it returns a <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop2">VDS_VOLUME_PROP2</a> structure instead of a <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a> structure.

## -parameters

### -param pVolumeProperties [out]

The address of the <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP2</a> structure 
      allocated and passed in by the caller. VDS allocates memory for the <b>pwszName</b> member 
      string. Callers must free the string by using the 
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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_PROPERTIES_INCOMPLETE</b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
</table>

## -remarks

This method retrieves the unique volume identifier for a volume. The structure that contains that identifier is <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop2">VDS_VOLUME_PROP2</a>, not <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a>.

Note that a unique volume identifier is not the same as a volume GUID path. To find the volume GUID paths for a volume, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf3-queryvolumeguidpathnames">IVdsVolumeMF3::QueryVolumeGuidPathnames</a> method.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume2">IVdsVolume2</a>