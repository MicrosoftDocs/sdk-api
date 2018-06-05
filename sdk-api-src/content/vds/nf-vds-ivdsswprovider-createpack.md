---
UID: NF:vds.IVdsSwProvider.CreatePack
title: IVdsSwProvider::CreatePack
author: windows-sdk-content
description: Creates a pack object.
old-location: base\ivdsswprovider_createpack.htm
old-project: VDS
ms.assetid: 2d711ed8-9101-4e68-b085-b5df01515b5d
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreatePack, CreatePack method [VDS], CreatePack method [VDS],IVdsSwProvider interface, IVdsSwProvider interface [VDS],CreatePack method, IVdsSwProvider.CreatePack, IVdsSwProvider::CreatePack, base.ivdsswprovider_createpack, vds/IVdsSwProvider::CreatePack
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
tech.root: 
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
-	IVdsSwProvider.CreatePack
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSwProvider::CreatePack


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates a pack object.


## -parameters




### -param ppPack [out]

The address of an <a href="https://msdn.microsoft.com/106989fe-d1dd-4c7f-b889-00a671c6e567">IVdsPack</a> interface. Callers must release the interface.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
<dt><b>VDS_E_ONLINE_PACK_EXISTS</b></dt>
<dt>0x80042464L</dt>
</dl>
</td>
<td width="60%">
Another dynamic pack exists with  <b>VDS_PS_ONLINE</b> status. Only one dynamic pack can have this status at a time.

</td>
</tr>
</table>
 




## -remarks



Use this method to create a pack before calling the <a href="https://msdn.microsoft.com/c7e85c4c-fb7c-48de-abd7-8d65ecb9a1fa">IVdsPack::MigrateDisks</a> method to convert disk formatting. When converting a basic disk to dynamic format,  pass either a new or existing pack as an argument to <b>MigrateDisks</b>. When converting a dynamic disk to basic format, use <b>CreatePack</b> to create a new, individual pack to hold the basic disk.




## -see-also




<a href="https://msdn.microsoft.com/106989fe-d1dd-4c7f-b889-00a671c6e567">IVdsPack</a>



<a href="https://msdn.microsoft.com/c7e85c4c-fb7c-48de-abd7-8d65ecb9a1fa">IVdsPack::MigrateDisks</a>



<a href="https://msdn.microsoft.com/0602d4d6-a31d-4425-ad21-a267c6e1dd7b">IVdsSwProvider</a>
 

 

