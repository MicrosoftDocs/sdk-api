---
UID: NF:vds.IVdsProviderSupport.GetVersionSupport
title: IVdsProviderSupport::GetVersionSupport (vds.h)
description: The IVdsProviderSupport::GetVersionSupport method (vds.h) returns a bitmask of values enumerated by VDS_VERSION_SUPPORT_FLAG with supported VDS interfaces.
helpviewer_keywords: ["GetVersionSupport","GetVersionSupport method","GetVersionSupport method","IVdsProviderSupport interface","IVdsProviderSupport interface","GetVersionSupport method","IVdsProviderSupport.GetVersionSupport","IVdsProviderSupport::GetVersionSupport","base.ivdsprovidersupport_getversionsupport","vds/IVdsProviderSupport::GetVersionSupport","vdshwprv/IVdsProviderSupport::GetVersionSupport"]
old-location: base\ivdsprovidersupport_getversionsupport.htm
tech.root: base
ms.assetid: c7527d29-7ab4-4f98-991b-411059e14237
ms.date: 08/05/2022
ms.keywords: GetVersionSupport, GetVersionSupport method, GetVersionSupport method,IVdsProviderSupport interface, IVdsProviderSupport interface,GetVersionSupport method, IVdsProviderSupport.GetVersionSupport, IVdsProviderSupport::GetVersionSupport, base.ivdsprovidersupport_getversionsupport, vds/IVdsProviderSupport::GetVersionSupport, vdshwprv/IVdsProviderSupport::GetVersionSupport
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsProviderSupport::GetVersionSupport
 - vds/IVdsProviderSupport::GetVersionSupport
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
 - IVdsProviderSupport.GetVersionSupport
---

# IVdsProviderSupport::GetVersionSupport


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a bitmask of values enumerated by 
    <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_version_support_flag">VDS_VERSION_SUPPORT_FLAG</a> indicating the versions 
    of the VDS interfaces supported by this provider. This method is implemented only by hardware providers.

## -parameters

### -param ulVersionSupport [out]

Address of a <b>ULONG</b> that receives a bitmask of one or more of the values enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_version_support_flag">VDS_VERSION_SUPPORT_FLAG</a> indicating the 
      versions of the VDS interfaces supported by the provider.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsprovidersupport">IVdsProviderSupport</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_version_support_flag">VDS_VERSION_SUPPORT_FLAG</a>
