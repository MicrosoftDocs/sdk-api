---
UID: NF:vdshwprv.IVdsAsync.Cancel
title: IVdsAsync::Cancel
author: windows-sdk-content
description: Cancels the asynchronous operation.
old-location: base\ivdsasync_cancel.htm
old-project: VDS
ms.assetid: 40940cb8-46b7-4483-9952-ab053c49dad7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: Cancel, Cancel method [VDS], Cancel method [VDS],IVdsAsync interface, IVdsAsync interface [VDS],Cancel method, IVdsAsync.Cancel, IVdsAsync::Cancel, base.ivdsasync_cancel, vds/IVdsAsync::Cancel, vdshwprv/IVdsAsync::Cancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsAsync.Cancel
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsAsync::Cancel


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Cancels the asynchronous 
   operation.


## -parameters






## -returns



This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
The method is not supported. Neither the basic provider nor the current dynamic provider support this 
        method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OPERATION_CANCELED</b></dt>
<dt>0x8004240DL</dt>
</dl>
</td>
<td width="60%">
The operation has already been canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANCEL_TOO_LATE</b></dt>
<dt>0x8004240CL</dt>
</dl>
</td>
<td width="60%">
The operation has progressed too far to cancel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_FILE_SYSTEM</b></dt>
<dt>0x80042425L</dt>
</dl>
</td>
<td width="60%">
The file system is incompatible with the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_MEDIA</b></dt>
<dt>0x80042426L</dt>
</dl>
</td>
<td width="60%">
The media is incompatible with this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ACCESS_DENIED</b></dt>
<dt>0x80042427L</dt>
</dl>
</td>
<td width="60%">
Access is denied. An application using VDS must run under the Backup Operator or Administrators group 
        account.

</td>
</tr>
</table>
 




## -remarks



Dynamic providers do not implement this method. The basic provider checks for this method only when cleaning 
    a disk and does not implement it for any other operation.




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>
 

 

