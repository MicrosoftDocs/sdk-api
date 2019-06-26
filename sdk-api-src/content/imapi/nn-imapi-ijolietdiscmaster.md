---
UID: NN:imapi.IJolietDiscMaster
title: IJolietDiscMaster (imapi.h)
author: windows-sdk-content
description: The IJolietDiscMaster interface enables the staging of a CD data disc.
old-location: imapi\ijolietdiscmaster.htm
tech.root: imapi
ms.assetid: e2269b68-1860-4afd-90f2-d61297f3fa9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IJolietDiscMaster, IJolietDiscMaster interface [IMAPI], IJolietDiscMaster interface [IMAPI],described, _win32_ijolietdiscmaster, base.ijolietdiscmaster, imapi.ijolietdiscmaster, imapi/IJolietDiscMaster
ms.topic: interface
f1_keywords: 
 - "imapi/IJolietDiscMaster"
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
ms.custom: 19H1
---

# IJolietDiscMaster interface


## -description


The 
<b>IJolietDiscMaster</b> interface enables the staging of a CD data disc. It represents one of the formats supported by <b>MSDiscMasterObj</b>, and it allows the creation of a single Track-at-Once data disc. The data is written to the disc with the Joliet and ISO-9660 file systems.

A temporary folder is constructed and added to the image. This can be repeated multiple times with the directory and file structures overlapping. The overlapping file structures appear seamlessly when read back. When the overwrite option is used, overlapping paths cause the last file added to show up in the directory, while the earlier files with conflicting names are still present on the disc but now not readable by normal means.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IJolietDiscMaster</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IJolietDiscMaster</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-adddata">AddData</a>
</td>
<td align="left" width="63%">
Adds directories and files to the image file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-getdatablocksize">GetDataBlockSize</a>
</td>
<td align="left" width="63%">
Retrieves the data block size in bytes (2048).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-getjolietproperties">GetJolietProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the Joliet interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks">GetTotalDataBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the total data blocks available on disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks">GetUsedDataBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the total data blocks staged in image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-ijolietdiscmaster-setjolietproperties">SetJolietProperties</a>
</td>
<td align="left" width="63%">
Sets the properties of the Joliet interface.

</td>
</tr>
</table> 

