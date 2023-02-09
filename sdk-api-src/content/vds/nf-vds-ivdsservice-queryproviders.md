---
UID: NF:vds.IVdsService.QueryProviders
title: IVdsService::QueryProviders (vds.h)
description: Returns an enumeration object containing a list of the hardware and software providers known to VDS.
helpviewer_keywords: ["IVdsService interface [VDS]","QueryProviders method","IVdsService.QueryProviders","IVdsService::QueryProviders","QueryProviders","QueryProviders method [VDS]","QueryProviders method [VDS]","IVdsService interface","base.ivdsservice_queryproviders","vds/IVdsService::QueryProviders"]
old-location: base\ivdsservice_queryproviders.htm
tech.root: base
ms.assetid: 55171eb1-6fec-4651-914c-88d23e8d7849
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],QueryProviders method, IVdsService.QueryProviders, IVdsService::QueryProviders, QueryProviders, QueryProviders method [VDS], QueryProviders method [VDS],IVdsService interface, base.ivdsservice_queryproviders, vds/IVdsService::QueryProviders
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
 - IVdsService::QueryProviders
 - vds/IVdsService::QueryProviders
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
 - IVdsService.QueryProviders
---

# IVdsService::QueryProviders


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an enumeration object containing a list of the hardware and software providers known to VDS.

## -parameters

### -param masks [in]

The provider mask enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_query_provider_flag">VDS_QUERY_PROVIDER_FLAG</a>. Callers can specify a software provider mask, a hardware provider mask, or both.

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the providers  as <a href="/windows/desktop/VDS/provider-object">provider objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the provider objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
The enumeration is returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>

## -remarks

To determine the provider type for hardware providers, call the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovidertype2-getprovidertype2">IVdsHwProviderType2::GetProviderType2</a> method or the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovidertype-getprovidertype">IVdsHwProviderType::GetProviderType</a> method for each provider object.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_hwprovider_type">VDS_HWPROVIDER_TYPE</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_query_provider_flag">VDS_QUERY_PROVIDER_FLAG</a>