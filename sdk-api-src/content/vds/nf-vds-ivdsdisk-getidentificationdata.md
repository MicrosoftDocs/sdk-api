---
UID: NF:vds.IVdsDisk.GetIdentificationData
title: IVdsDisk::GetIdentificationData (vds.h)
description: Retrieves information that uniquely identifies a disk.
helpviewer_keywords: ["GetIdentificationData","GetIdentificationData method [VDS]","GetIdentificationData method [VDS]","IVdsDisk interface","IVdsDisk interface [VDS]","GetIdentificationData method","IVdsDisk.GetIdentificationData","IVdsDisk::GetIdentificationData","base.ivdsdisk_getidentificationdata","vds/IVdsDisk::GetIdentificationData"]
old-location: base\ivdsdisk_getidentificationdata.htm
tech.root: base
ms.assetid: 400fa102-f98a-4bc1-919c-858c135a5b93
ms.date: 12/05/2018
ms.keywords: GetIdentificationData, GetIdentificationData method [VDS], GetIdentificationData method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],GetIdentificationData method, IVdsDisk.GetIdentificationData, IVdsDisk::GetIdentificationData, base.ivdsdisk_getidentificationdata, vds/IVdsDisk::GetIdentificationData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsDisk::GetIdentificationData
 - vds/IVdsDisk::GetIdentificationData
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
 - IVdsDisk.GetIdentificationData
---

# IVdsDisk::GetIdentificationData


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves information that uniquely identifies a disk.

## -parameters

### -param pLunInfo [out]

The address of the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure allocated and passed in by the caller. VDS allocates memory for the <b>m_szVendorId</b>, 
      <b>m_szProductId</b>, <b>m_szProductRevision</b>, 
      and <b>m_szSerialNumber</b> member strings, as well as the <b>m_pbPort</b> and   <b>m_pbAddress</b> member strings of each element in the array of <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_interconnect">VDS_INTERCONNECT</a> structures. 
      Callers must free the strings by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>