---
UID: NF:imapi2fs.IFileSystemImage3.put_CreateRedundantUdfMetadataFiles
title: IFileSystemImage3::put_CreateRedundantUdfMetadataFiles
author: windows-sdk-content
description: Sets the property that specifies if the UDF Metadata will be redundant in the file system image.
old-location: imapi\ifilesystemimage3_put_createredundantudfmetadatafiles.htm
tech.root: imapi
ms.assetid: 594ef77e-57be-4ef0-9eba-3e6fc0340f6e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFileSystemImage3 interface [IMAPI],put_CreateRedundantUdfMetadataFiles method, IFileSystemImage3.put_CreateRedundantUdfMetadataFiles, IFileSystemImage3::put_CreateRedundantUdfMetadataFiles, imapi.ifilesystemimage3_put_createredundantudfmetadatafiles, imapi2fs/IFileSystemImage3::put_CreateRedundantUdfMetadataFiles, put_CreateRedundantUdfMetadataFiles, put_CreateRedundantUdfMetadataFiles method [IMAPI], put_CreateRedundantUdfMetadataFiles method [IMAPI],IFileSystemImage3 interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IFileSystemImage3.put_CreateRedundantUdfMetadataFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2fs.h
: 
- IFileSystemImage3.put_CreateRedundantUdfMetadataFiles
: 
---

# IFileSystemImage3::put_CreateRedundantUdfMetadataFiles


## -description


Sets the property that specifies  if the UDF Metadata will be redundant in the  file system image.


## -parameters




### -param newVal [in]

Specifies if the UDF metadata is redundant in the resultant file system image or not. A value of <b>VARIANT_TRUE</b> indicates that UDF metadata will be redundant; otherwise, <b>VARIANT_FALSE</b>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</b></dt>
<dt>Value: 0x00AAB15FL</dt>
</dl>
</td>
<td width="60%">
Option changed, but the feature is not supported for the implemented file system revision, and the image will be created without this feature.

</td>
</tr>
</table>
 




## -remarks



The UDF metadata redundancy option affects only UDF revisions 2.50 and higher. If this method is invoked for a file system object that does not contain the required UDF revision in the list of file systems enabled for creation in the resultant image this method returns <b>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</b>.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/ffe343fa-2837-41f7-b7e0-097788fb5d4e">IFileSystemImage3</a>
 

 

