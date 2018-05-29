---
UID: NF:vds.IVdsRemovable.Eject
title: IVdsRemovable::Eject
author: windows-sdk-content
description: Ejects the media from the current device.
old-location: base\ivdsremovable_eject.htm
old-project: VDS
ms.assetid: c77885bd-67af-41c1-9190-e0148c7b7ed5
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: Eject, Eject method [VDS], Eject method [VDS],IVdsRemovable interface, IVdsRemovable interface [VDS],Eject method, IVdsRemovable.Eject, IVdsRemovable::Eject, base.ivdsremovable_eject, vds/IVdsRemovable::Eject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsRemovable.Eject
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsRemovable::Eject


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Ejects the media from the current device.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The media was ejected successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DEVICE_IN_USE</b></dt>
<dt>0x80042413L</dt>
</dl>
</td>
<td width="60%">
The call to the device failed because the device was performing another operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/86dcd76a-0de0-42f4-9360-87cf7ca4ebf6">IVdsRemovable</a>



<a href="https://msdn.microsoft.com/6a56be84-ddf3-4c82-9465-4cb683e993f6">IVdsRemovable::QueryMedia</a>
 

 

