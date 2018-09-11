---
UID: NN:imapi.IJolietDiscMaster
title: IJolietDiscMaster
author: windows-sdk-content
description: The IJolietDiscMaster interface enables the staging of a CD data disc.
old-location: imapi\ijolietdiscmaster.htm
tech.root: imapi
ms.assetid: e2269b68-1860-4afd-90f2-d61297f3fa9b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IJolietDiscMaster, IJolietDiscMaster interface [IMAPI], IJolietDiscMaster interface [IMAPI],described, _win32_ijolietdiscmaster, base.ijolietdiscmaster, imapi.ijolietdiscmaster, imapi/IJolietDiscMaster
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IJolietDiscMaster
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IJolietDiscMaster interface


## -description


The 
<b>IJolietDiscMaster</b> interface enables the staging of a CD data disc. It represents one of the formats supported by <b>MSDiscMasterObj</b>, and it allows the creation of a single Track-at-Once data disc. The data is written to the disc with the Joliet and ISO-9660 file systems.

A temporary folder is constructed and added to the image. This can be repeated multiple times with the directory and file structures overlapping. The overlapping file structures appear seamlessly when read back. When the overwrite option is used, overlapping paths cause the last file added to show up in the directory, while the earlier files with conflicting names are still present on the disc but now not readable by normal means.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IJolietDiscMaster</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IJolietDiscMaster</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IJolietDiscMaster</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91517103-71c5-450c-9d93-584f94cd2c45">AddData</a>
</td>
<td align="left" width="63%">
Adds directories and files to the image file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84bb0330-770d-44ab-8829-e81616f7c805">GetDataBlockSize</a>
</td>
<td align="left" width="63%">
Retrieves the data block size in bytes (2048).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/660657b3-b378-4c16-9294-89309e4da569">GetJolietProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the Joliet interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa5df4de-eecc-406b-a38d-939e7b631fc8">GetTotalDataBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the total data blocks available on disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01bde64a-3d91-4830-bd93-f3fe6b109264">GetUsedDataBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the total data blocks staged in image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/467f8fb8-2a82-46d2-b304-3c3a600a9c63">SetJolietProperties</a>
</td>
<td align="left" width="63%">
Sets the properties of the Joliet interface.

</td>
</tr>
</table> 

