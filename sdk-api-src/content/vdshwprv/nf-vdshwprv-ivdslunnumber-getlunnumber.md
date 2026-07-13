---
UID: NF:vdshwprv.IVdsLunNumber.GetLunNumber
title: IVdsLunNumber::GetLunNumber (vdshwprv.h)
description: The IVdsLunNumber::GetLunNumber (vdshwprv.h) method retrieves the LUN number for a LUN.
helpviewer_keywords: ["GetLunNumber","GetLunNumber method","GetLunNumber method","IVdsLunNumber interface","IVdsLunNumber interface","GetLunNumber method","IVdsLunNumber.GetLunNumber","IVdsLunNumber::GetLunNumber","base.ivdslunnumber_getlunnumber","vds/IVdsLunNumber::GetLunNumber","vdshwprv/IVdsLunNumber::GetLunNumber"]
old-location: base\ivdslunnumber_getlunnumber.htm
tech.root: base
ms.assetid: 79aa7dc1-ef46-4b6d-8088-e42839625a16
ms.date: 08/08/2022
ms.keywords: GetLunNumber, GetLunNumber method, GetLunNumber method,IVdsLunNumber interface, IVdsLunNumber interface,GetLunNumber method, IVdsLunNumber.GetLunNumber, IVdsLunNumber::GetLunNumber, base.ivdslunnumber_getlunnumber, vds/IVdsLunNumber::GetLunNumber, vdshwprv/IVdsLunNumber::GetLunNumber
req.header: vdshwprv.h
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
 - IVdsLunNumber::GetLunNumber
 - vdshwprv/IVdsLunNumber::GetLunNumber
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
 - IVdsLunNumber.GetLunNumber
---

# IVdsLunNumber::GetLunNumber


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the LUN number for a LUN.

## -parameters

### -param pulLunNumber [out]

The address of a  variable that receives the LUN number. This value is required and cannot be <b>NULL</b>.

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
The method completed successfully.

</td>
</tr>
</table>

## -remarks

This method returns the LUN number that the VDS hardware provider assigned to the LUN. This number identifies the LUN  within the disk array.  It is not the same as the "Logical Unit Number" in the disk's SCSI address. Each LUN in the disk array is assigned exactly one LUN number.

This method exists because the DiskRAID utility assigns its own index to each LUN when it enumerates the LUNs in a subsystem. But these indexes can change each time DiskRAID is run, if the hardware provider enumerates the LUNs in a different order. This can be confusing to end users. For disk arrays that have their own (provider-assigned) LUN numbers, this method gives the caller the ability to map the LUN numbers to the LUN indexes that are assigned by DiskRAID.

If a subsystem supports LUN numbering, it can indicate this support by setting the <b>VDS_SF_SUPPORTS_LUN_NUMBER</b> flag in the <b>ulFlags</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> or <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop2">VDS_SUB_SYSTEM_PROP2</a> structure. For more information about this flag, see the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunnumber">IVdsLunNumber</a>
