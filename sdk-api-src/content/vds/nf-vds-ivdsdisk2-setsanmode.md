---
UID: NF:vds.IVdsDisk2.SetSANMode
title: IVdsDisk2::SetSANMode
author: windows-sdk-content
description: Sets the SAN mode of a disk to offline or online.
old-location: base\ivdsdisk2_setsanmode.htm
old-project: VDS
ms.assetid: 17bdb6f4-7d85-4aa6-b89b-a752332cc224
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsDisk2 interface,SetSANMode method, IVdsDisk2.SetSANMode, IVdsDisk2::SetSANMode, SetSANMode, SetSANMode method, SetSANMode method,IVdsDisk2 interface, base.ivdsdisk2_setsanmode, vds/IVdsDisk2::SetSANMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IVdsDisk2.SetSANMode
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDisk2::SetSANMode


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Sets the SAN mode of a disk to offline or online.<div class="alert"><b>Note</b>  Starting with Windows Vista with Service Pack 1 (SP1), this method is superseded by the <a href="https://msdn.microsoft.com/b3366bc7-18ca-4a90-b4e7-e6213a7cc002">IVdsDiskOnline::Online</a> and <a href="https://msdn.microsoft.com/3f27dd46-2fa1-4522-9d35-db78255c6d11">IVdsDiskOnline::Offline</a> methods.</div>
<div> </div>



## -parameters




### -param bEnable [in]

Specify <b>TRUE</b> for online or <b>FALSE</b> for offline.


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




<a href="https://msdn.microsoft.com/9fb8a08e-412d-415a-aa27-cc0180599903">IVdsDisk2</a>
 

 

