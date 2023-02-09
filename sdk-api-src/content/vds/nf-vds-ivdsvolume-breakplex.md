---
UID: NF:vds.IVdsVolume.BreakPlex
title: IVdsVolume::BreakPlex (vds.h)
description: Removes a specified plex from the current volume.
helpviewer_keywords: ["BreakPlex","BreakPlex method [VDS]","BreakPlex method [VDS]","IVdsVolume interface","IVdsVolume interface [VDS]","BreakPlex method","IVdsVolume.BreakPlex","IVdsVolume::BreakPlex","base.ivdsvolume_breakplex","vds/IVdsVolume::BreakPlex"]
old-location: base\ivdsvolume_breakplex.htm
tech.root: base
ms.assetid: c7e42aa4-3233-40e9-b537-043eecd192ad
ms.date: 12/05/2018
ms.keywords: BreakPlex, BreakPlex method [VDS], BreakPlex method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],BreakPlex method, IVdsVolume.BreakPlex, IVdsVolume::BreakPlex, base.ivdsvolume_breakplex, vds/IVdsVolume::BreakPlex
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
 - IVdsVolume::BreakPlex
 - vds/IVdsVolume::BreakPlex
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
 - IVdsVolume.BreakPlex
---

# IVdsVolume::BreakPlex


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Removes a specified 
   plex from the current volume. The interface pointer for the new 
   <a href="/windows/desktop/VDS/volume-object">volume object</a> can be retrieved by calling 
   <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> through the 
   <i>ppAsync</i> parameter. The 
   <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure returned contains the volume 
   object interface pointer in the <b>bvp.pVolumeUnk</b> member.

## -parameters

### -param plexId [in]

The GUID of the plex to be broken.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, 
      which VDS initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or 
      query the status of the operation.

If you call <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> on this method and a success HRESULT value is returned, 
      you must release the interfaces returned in the 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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
The plex was broken successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_ONLINE</b></dt>
<dt>0x8004243DL</dt>
</dl>
</td>
<td width="60%">
The volume is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_A_MIRROR</b></dt>
<dt>0x80042445L</dt>
</dl>
</td>
<td width="60%">
The volume is not a mirror.

</td>
</tr>
</table>

## -remarks

This operation is not valid for basic volumes, which have exactly one plex.

Use this method to break a mirror. The broken plex becomes a new volume. If the remaining plex is stale or 
    missing, VDS stops the operation and returns an error. Note that VDS dismounts the volume during the 
    operation.

A boot or system plex—essentially, the plex used to boot the computer—is not valid for 
    <b>plexId</b>. When passed such a plex, VDS stops the operation and returns an error.

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> 
     interface for this method, regardless of whether the call initiates an asynchronous operation.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a>