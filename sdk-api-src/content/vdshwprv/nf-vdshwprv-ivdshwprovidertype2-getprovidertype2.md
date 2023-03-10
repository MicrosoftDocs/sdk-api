---
UID: NF:vdshwprv.IVdsHwProviderType2.GetProviderType2
title: IVdsHwProviderType2::GetProviderType2 (vdshwprv.h)
description: The IVdsHwProviderType2::GetProviderType2 (vdshwprv.h) method retrieves the type of the hardware provider.
helpviewer_keywords: ["GetProviderType2","GetProviderType2 method","GetProviderType2 method","IVdsHwProviderType2 interface","IVdsHwProviderType2 interface","GetProviderType2 method","IVdsHwProviderType2.GetProviderType2","IVdsHwProviderType2::GetProviderType2","base.ivdshwprovidertype2_getprovidertype2","vds/IVdsHwProviderType2::GetProviderType2","vdshwprv/IVdsHwProviderType2::GetProviderType2"]
old-location: base\ivdshwprovidertype2_getprovidertype2.htm
tech.root: base
ms.assetid: 9a75e6af-fd3d-4770-bc6d-31ad4d995eee
ms.date: 08/08/2022
ms.keywords: GetProviderType2, GetProviderType2 method, GetProviderType2 method,IVdsHwProviderType2 interface, IVdsHwProviderType2 interface,GetProviderType2 method, IVdsHwProviderType2.GetProviderType2, IVdsHwProviderType2::GetProviderType2, base.ivdshwprovidertype2_getprovidertype2, vds/IVdsHwProviderType2::GetProviderType2, vdshwprv/IVdsHwProviderType2::GetProviderType2
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
 - IVdsHwProviderType2::GetProviderType2
 - vdshwprv/IVdsHwProviderType2::GetProviderType2
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
 - IVdsHwProviderType2.GetProviderType2
---

# IVdsHwProviderType2::GetProviderType2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Not implemented.

Retrieves the type of the hardware provider. If the provider wants to maintain backward compatibility with clients that do not recognize the new provider type, the provider should continue to return the old provider type in the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovidertype-getprovidertype">IVdsHwProviderType::GetProviderType</a> method.<div class="alert"><b>Note</b>  This method is identical to <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovidertype-getprovidertype">IVdsHwProviderType::GetProviderType</a> and should not be used.</div>
<div> </div>

## -parameters

### -param pType [out]

A pointer to a caller-allocated variable that receives a <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_hwprovider_type">VDS_HWPROVIDER_TYPE</a> enumeration value that specifies the hardware provider type. This parameter is required and cannot be <b>NULL</b>.

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
The hardware provider type was returned successfully.

</td>
</tr>
</table>

## -remarks

If the provider object supports the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwprovidertype2">IVdsHwProviderType2</a> interface, the server must call the <b>GetProviderType2</b> method on the provider object to retrieve the provider type and then return an HRESULT indicating failure or success.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwprovidertype2">IVdsHwProviderType2</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovidertype-getprovidertype">IVdsHwProviderType::GetProviderType</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">IVdsService::QueryProviders</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_hwprovider_type">VDS_HWPROVIDER_TYPE</a>
