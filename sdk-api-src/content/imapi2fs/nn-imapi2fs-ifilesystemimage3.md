---
UID: NN:imapi2fs.IFileSystemImage3
title: IFileSystemImage3
author: windows-sdk-content
description: Use this interface to set or check the metadata and metadata mirror files in a UDF file system (rev 2.50 and later) to determine redundancy.
old-location: imapi\ifilesystemimage3.htm
tech.root: imapi
ms.assetid: ffe343fa-2837-41f7-b7e0-097788fb5d4e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFileSystemImage3, IFileSystemImage3 interface [IMAPI], IFileSystemImage3 interface [IMAPI],described, imapi.ifilesystemimage3, imapi2fs/IFileSystemImage3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage3 interface


## -description


Use this interface to set or check the metadata and metadata mirror files in a UDF file system (rev 2.50 and later) to determine  redundancy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemImage3</b> interface inherits from <a href="https://msdn.microsoft.com/c38995b7-6f32-4489-bb6c-0e3561b11f81">IFileSystemImage2</a>. <b>IFileSystemImage3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemImage3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d71e997f-e6d6-414b-b89e-73a486f29619">get_CreateRedundantUdfMetadataFiles</a>
</td>
<td align="left" width="63%">
Retrieves the option that indicates whether UDF metadata will be redundant in the file system image

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0594c2e4-30ba-4d02-948e-09ec6a4ec352">ProbeSpecificFileSystem</a>
</td>
<td align="left" width="63%">
Determines if a specific file system on the current media is appendable through the IMAPI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/594ef77e-57be-4ef0-9eba-3e6fc0340f6e">put_CreateRedundantUdfMetadataFiles</a>
</td>
<td align="left" width="63%">
Sets the option that indicates whether UDF metadata will be redundant in the  file system image

</td>
</tr>
</table> 


## -remarks



If the metadata and metadata mirror files are set for redundancy, IMAPI  creates identical copies of each in the file system image, which results in increased level of fault tolerance. In a scenario where the metadata files are not set for redundancy, IMAPI only creates a single copy in the file system image, which can save several MB of space on the burned disc.

The metadata redundancy option is set to <b>TRUE</b> by default.

<b>IFileSystemImage3</b> is the default interface of <b>MsftFileSystemImage3</b> objects.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/c38995b7-6f32-4489-bb6c-0e3561b11f81">IFileSystemImage2</a>
 

 

