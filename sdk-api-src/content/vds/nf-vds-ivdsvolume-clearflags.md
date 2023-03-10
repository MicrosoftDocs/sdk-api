---
UID: NF:vds.IVdsVolume.ClearFlags
title: IVdsVolume::ClearFlags (vds.h)
description: Clears the volume flags.
helpviewer_keywords: ["ClearFlags","ClearFlags method [VDS]","ClearFlags method [VDS]","IVdsVolume interface","IVdsVolume interface [VDS]","ClearFlags method","IVdsVolume.ClearFlags","IVdsVolume::ClearFlags","base.ivdsvolume_clearflags","vds/IVdsVolume::ClearFlags"]
old-location: base\ivdsvolume_clearflags.htm
tech.root: base
ms.assetid: 970dcd4a-ac06-4e2d-969c-82c5dabd0019
ms.date: 12/05/2018
ms.keywords: ClearFlags, ClearFlags method [VDS], ClearFlags method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],ClearFlags method, IVdsVolume.ClearFlags, IVdsVolume::ClearFlags, base.ivdsvolume_clearflags, vds/IVdsVolume::ClearFlags
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
 - IVdsVolume::ClearFlags
 - vds/IVdsVolume::ClearFlags
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
 - IVdsVolume.ClearFlags
---

# IVdsVolume::ClearFlags


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Clears the volume flags.

## -parameters

### -param ulFlags [in]

The flags enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a>. Callers can clear the following flags: 

<b>VDS_VF_LBN_REMAP_ENABLED</b>
<b>VDS_VF_HIDDEN</b>
<b>VDS_VF_READONLY</b>
<b>VDS_VF_NO_DEFAULT_DRIVE_LETTER</b>
<b>VDS_VF_INSTALLABLE</b>
<b>VDS_VF_SHADOW_COPY</b>

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
The flags were cleared successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_REVERT_ON_CLOSE_MISMATCH</b></dt>
<dt>0x80042462L</dt>
</dl>
</td>
<td width="60%">
The flags to be cleared do not match the flags set previously with the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-setflags">SetFlags</a> method  and <i>bRevertOnClose</i> is set to <b>TRUE</b>.

</td>
</tr>
</table>

## -remarks

To create a boot volume on a dynamic disk, you must set the <b>VDS_VF_INSTALLABLE</b> flag for the volume and then format the volume by calling the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-format">IVdsVolumeMF::Format</a> method.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-setflags">IVdsVolume::SetFlags</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a>