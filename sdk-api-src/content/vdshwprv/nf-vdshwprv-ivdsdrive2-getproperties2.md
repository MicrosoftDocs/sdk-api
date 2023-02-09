---
UID: NF:vdshwprv.IVdsDrive2.GetProperties2
title: IVdsDrive2::GetProperties2 (vdshwprv.h)
description: The IVdsDrive2::GetProperties2 (vdshwprv.h) method returns the properties of a drive object.
helpviewer_keywords: ["GetProperties2","GetProperties2 method","GetProperties2 method","IVdsDrive2 interface","IVdsDrive2 interface","GetProperties2 method","IVdsDrive2.GetProperties2","IVdsDrive2::GetProperties2","base.ivdsdrive2_getproperties2","vds/IVdsDrive2::GetProperties2","vdshwprv/IVdsDrive2::GetProperties2"]
old-location: base\ivdsdrive2_getproperties2.htm
tech.root: base
ms.assetid: 635957be-780f-4dee-8d70-b7fc37fecd5c
ms.date: 08/08/2022
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsDrive2 interface, IVdsDrive2 interface,GetProperties2 method, IVdsDrive2.GetProperties2, IVdsDrive2::GetProperties2, base.ivdsdrive2_getproperties2, vds/IVdsDrive2::GetProperties2, vdshwprv/IVdsDrive2::GetProperties2
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsDrive2::GetProperties2
 - vdshwprv/IVdsDrive2::GetProperties2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsDrive2.GetProperties2
---

# IVdsDrive2::GetProperties2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of a drive object.

## -parameters

### -param pDriveProp2 [out]

The address of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop2">VDS_DRIVE_PROP2</a> structure 
      allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszFriendlyName</b> and <b>pwszIdentification</b> member strings. 
      Callers must free the strings by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function. This parameter is required and cannot be <b>NULL</b>.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used.

## -remarks

This method must return zero (S_OK) to indicate success, or an implementation-specific nonzero error code to indicate failure.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsdrive2">IVdsDrive2</a>
