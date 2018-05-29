---
UID: NF:vds.IVdsDisk.ConvertStyle
title: IVdsDisk::ConvertStyle
author: windows-sdk-content
description: Converts the partition style of an empty disk from one style to another.
old-location: base\ivdsdisk_convertstyle.htm
old-project: VDS
ms.assetid: 38c129cd-8e60-4e4a-b22b-26c69c68fe89
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ConvertStyle, ConvertStyle method [VDS], ConvertStyle method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],ConvertStyle method, IVdsDisk.ConvertStyle, IVdsDisk::ConvertStyle, base.ivdsdisk_convertstyle, vds/IVdsDisk::ConvertStyle
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
-	IVdsDisk.ConvertStyle
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDisk::ConvertStyle


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Converts the partition style of an empty disk from one style to another.


## -parameters




### -param NewStyle [in]

The partition styles enumerated by <a href="https://msdn.microsoft.com/31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb">VDS_PARTITION_STYLE</a>.


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
The conversion completed successfully.

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
The disk style cannot be converted, as is the case for 1394 or USB disks and unallocated disks.

</td>
</tr>
</table>
 




## -remarks



An empty disk contains no user data, OEM partitions, ESP partitions, or unknown partitions. Only LDM metadata partitions and MSR partitions are valid on an empty disk.




## -see-also




<a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a>



<a href="https://msdn.microsoft.com/5c484155-df73-4007-a137-998c7f1c5a7c">VDS_PARTITION_INFO_GPT</a>



<a href="https://msdn.microsoft.com/d14a852f-8a78-4631-a288-476701321ac2">VDS_PARTITION_INFO_MBR</a>



<a href="https://msdn.microsoft.com/31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb">VDS_PARTITION_STYLE</a>
 

 

