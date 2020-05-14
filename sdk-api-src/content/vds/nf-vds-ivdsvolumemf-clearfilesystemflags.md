---
UID: NF:vds.IVdsVolumeMF.ClearFileSystemFlags
title: IVdsVolumeMF::ClearFileSystemFlags (vds.h)
description: Clears the file-system flags.helpviewer_keywords: ["ClearFileSystemFlags","ClearFileSystemFlags method [VDS]","ClearFileSystemFlags method [VDS]","IVdsVolumeMF interface","IVdsVolumeMF interface [VDS]","ClearFileSystemFlags method","IVdsVolumeMF.ClearFileSystemFlags","IVdsVolumeMF::ClearFileSystemFlags","base.ivdsvolumemf_clearfilesystemflags","vds/IVdsVolumeMF::ClearFileSystemFlags"]
old-location: base\ivdsvolumemf_clearfilesystemflags.htm
tech.root: VDS
ms.assetid: f3b02b4a-109c-419f-94c1-fc2f15ea5291
ms.date: 12/05/2018
ms.keywords: ClearFileSystemFlags, ClearFileSystemFlags method [VDS], ClearFileSystemFlags method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],ClearFileSystemFlags method, IVdsVolumeMF.ClearFileSystemFlags, IVdsVolumeMF::ClearFileSystemFlags, base.ivdsvolumemf_clearfilesystemflags, vds/IVdsVolumeMF::ClearFileSystemFlags
f1_keywords:
- vds/IVdsVolumeMF.ClearFileSystemFlags
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsVolumeMF.ClearFileSystemFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumeMF::ClearFileSystemFlags


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Clears the file-system flags.


## -parameters




### -param ulFlags [in]

The flags enumerated by <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-vds_file_system_flag">VDS_FILE_SYSTEM_FLAG</a>. Callers can clear the <b>VDS_FPF_COMPRESSED</b> flag.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_OPERATION</b></dt>
<dt>0x80042415L</dt>
</dl>
</td>
<td width="60%">
The volume is hidden. This method cannot be called on a hidden volume.

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
The volume failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PACK_OFFLINE</b></dt>
<dt>0x80042444L</dt>
</dl>
</td>
<td width="60%">
The pack containing the volume is not accessible.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-setfilesystemflags">IVdsVolumeMF::SetFileSystemFlags</a>
 

 

