---
UID: NF:vds.IVdsDisk2.SetSANMode
title: IVdsDisk2::SetSANMode (vds.h)
description: Sets the SAN mode of a disk to offline or online.
helpviewer_keywords: ["IVdsDisk2 interface","SetSANMode method","IVdsDisk2.SetSANMode","IVdsDisk2::SetSANMode","SetSANMode","SetSANMode method","SetSANMode method","IVdsDisk2 interface","base.ivdsdisk2_setsanmode","vds/IVdsDisk2::SetSANMode"]
old-location: base\ivdsdisk2_setsanmode.htm
tech.root: base
ms.assetid: 17bdb6f4-7d85-4aa6-b89b-a752332cc224
ms.date: 12/05/2018
ms.keywords: IVdsDisk2 interface,SetSANMode method, IVdsDisk2.SetSANMode, IVdsDisk2::SetSANMode, SetSANMode, SetSANMode method, SetSANMode method,IVdsDisk2 interface, base.ivdsdisk2_setsanmode, vds/IVdsDisk2::SetSANMode
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVdsDisk2::SetSANMode
 - vds/IVdsDisk2::SetSANMode
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
 - IVdsDisk2.SetSANMode
---

# IVdsDisk2::SetSANMode


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the SAN mode of a disk to offline or online.<div class="alert"><b>Note</b>  Starting with Windows Vista with Service Pack 1 (SP1), this method is superseded by the <a href="/windows/desktop/api/vds/nf-vds-ivdsdiskonline-online">IVdsDiskOnline::Online</a> and <a href="/windows/desktop/api/vds/nf-vds-ivdsdiskonline-offline">IVdsDiskOnline::Offline</a> methods.</div>
<div> </div>

## -parameters

### -param bEnable [in]

Specify <b>TRUE</b> for online or <b>FALSE</b> for offline.

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
The SAN mode was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_FAILED_TO_OFFLINE_DISK</b></dt>
<dt>0x80042597L</dt>
</dl>
</td>
<td width="60%">
The offline operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_FAILED_TO_ONLINE_DISK</b></dt>
<dt>0x80042596L</dt>
</dl>
</td>
<td width="60%">
The online operation failed.

</td>
</tr>
</table>

## -remarks

Setting the SAN mode of a disk to offline is called "offlining" the disk. Setting it to online is called "onlining" the disk.

<b>Windows Vista:  </b>Setting the SAN mode of a disk to offline also makes the disk read-only. Setting it to online also makes the disk read-write.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk2">IVdsDisk2</a>