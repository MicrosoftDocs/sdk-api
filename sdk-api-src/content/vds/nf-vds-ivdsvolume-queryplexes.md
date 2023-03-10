---
UID: NF:vds.IVdsVolume.QueryPlexes
title: IVdsVolume::QueryPlexes (vds.h)
description: Returns an object that enumerates the plexes of the volume.
helpviewer_keywords: ["IVdsVolume interface [VDS]","QueryPlexes method","IVdsVolume.QueryPlexes","IVdsVolume::QueryPlexes","QueryPlexes","QueryPlexes method [VDS]","QueryPlexes method [VDS]","IVdsVolume interface","base.ivdsvolume_queryplexes","vds/IVdsVolume::QueryPlexes"]
old-location: base\ivdsvolume_queryplexes.htm
tech.root: base
ms.assetid: 33fc5b7c-4d05-4ec7-8d03-631c6d9f2f34
ms.date: 12/05/2018
ms.keywords: IVdsVolume interface [VDS],QueryPlexes method, IVdsVolume.QueryPlexes, IVdsVolume::QueryPlexes, QueryPlexes, QueryPlexes method [VDS], QueryPlexes method [VDS],IVdsVolume interface, base.ivdsvolume_queryplexes, vds/IVdsVolume::QueryPlexes
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
 - IVdsVolume::QueryPlexes
 - vds/IVdsVolume::QueryPlexes
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
 - IVdsVolume.QueryPlexes
---

# IVdsVolume::QueryPlexes


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an object that enumerates  the plexes of the volume.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the plexes  as <a href="/windows/desktop/VDS/volume-plex-object">volume plex objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the volume  plex objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>