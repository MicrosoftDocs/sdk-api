---
UID: NF:vds.IVdsLunPlex.ApplyHints
title: IVdsLunPlex::ApplyHints (vds.h)
description: The IVdsLunPlex::ApplyHints method (vds.h) applies a new set of hints to the LUN plex. Hints applied to a plex affect neither the LUN nor its other plexes.
helpviewer_keywords: ["ApplyHints","ApplyHints method [VDS]","ApplyHints method [VDS]","IVdsLunPlex interface","IVdsLunPlex interface [VDS]","ApplyHints method","IVdsLunPlex.ApplyHints","IVdsLunPlex::ApplyHints","base.ivdslunplex_applyhints","vds/IVdsLunPlex::ApplyHints","vdshwprv/IVdsLunPlex::ApplyHints"]
old-location: base\ivdslunplex_applyhints.htm
tech.root: base
ms.assetid: 66299644-4b70-4cd3-ae99-4d4084c3c3c5
ms.date: 08/05/2022
ms.keywords: ApplyHints, ApplyHints method [VDS], ApplyHints method [VDS],IVdsLunPlex interface, IVdsLunPlex interface [VDS],ApplyHints method, IVdsLunPlex.ApplyHints, IVdsLunPlex::ApplyHints, base.ivdslunplex_applyhints, vds/IVdsLunPlex::ApplyHints, vdshwprv/IVdsLunPlex::ApplyHints
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
 - IVdsLunPlex::ApplyHints
 - vds/IVdsLunPlex::ApplyHints
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
 - IVdsLunPlex.ApplyHints
---

# IVdsLunPlex::ApplyHints


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Applies a new set of hints to the LUN plex. Hints applied to a plex affect neither the LUN nor its other plexes.

## -parameters

### -param pHints [in]

Pointer to the hints to be applied to the LUN plex. See the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure. Only fields relevant to a LUN plex are expected to be set; irrelevant fields are ignored.

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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information about the array. Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method followed by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The LUN plex is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The LUN plex is in a failed state, and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>

## -remarks

Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryhints">IVdsLunPlex::QueryHints</a> method to get the current hints for the LUN plex.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunplex">IVdsLunPlex</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryhints">IVdsLunPlex::QueryHints</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a>
