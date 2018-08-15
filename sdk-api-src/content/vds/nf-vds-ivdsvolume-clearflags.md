---
UID: NF:vds.IVdsVolume.ClearFlags
title: IVdsVolume::ClearFlags
author: windows-sdk-content
description: Clears the volume flags.
old-location: base\ivdsvolume_clearflags.htm
old-project: vds
ms.assetid: 970dcd4a-ac06-4e2d-969c-82c5dabd0019
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ClearFlags, ClearFlags method [VDS], ClearFlags method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],ClearFlags method, IVdsVolume.ClearFlags, IVdsVolume::ClearFlags, base.ivdsvolume_clearflags, vds/IVdsVolume::ClearFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
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
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolume::ClearFlags


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Clears the volume flags.


## -parameters




### -param ulFlags [in]

The flags enumerated by <a href="https://msdn.microsoft.com/3a59cc61-1efe-4027-9aca-a785a5cfaef5">VDS_VOLUME_FLAG</a>. Callers can clear the following flags: 

<b>VDS_VF_LBN_REMAP_ENABLED</b>
<b>VDS_VF_HIDDEN</b>
<b>VDS_VF_READONLY</b>
<b>VDS_VF_NO_DEFAULT_DRIVE_LETTER</b>
<b>VDS_VF_INSTALLABLE</b>
<b>VDS_VF_SHADOW_COPY</b>

## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The flags to be cleared do not match the flags set previously with the <a href="https://msdn.microsoft.com/f426b089-6c5f-4ab4-aa92-127e24cb57b1">SetFlags</a> method  and <i>bRevertOnClose</i> is set to <b>TRUE</b>.

</td>
</tr>
</table>
 




## -remarks



To create a boot volume on a dynamic disk, you must set the <b>VDS_VF_INSTALLABLE</b> flag for the volume and then format the volume by calling the <a href="https://msdn.microsoft.com/8203ac16-99af-4962-bafc-12c0d238d062">IVdsVolumeMF::Format</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>



<a href="https://msdn.microsoft.com/f426b089-6c5f-4ab4-aa92-127e24cb57b1">IVdsVolume::SetFlags</a>



<a href="https://msdn.microsoft.com/3a59cc61-1efe-4027-9aca-a785a5cfaef5">VDS_VOLUME_FLAG</a>
 

 

