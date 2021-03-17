---
UID: NF:imapi2fs.IFsiDirectoryItem2.AddTreeWithNamedStreams
title: IFsiDirectoryItem2::AddTreeWithNamedStreams (imapi2fs.h)
description: Adds the contents of a directory tree along with named streams associated with all files to the file system image.
helpviewer_keywords: ["AddTreeWithNamedStreams","AddTreeWithNamedStreams method [IMAPI]","AddTreeWithNamedStreams method [IMAPI]","IFsiDirectoryItem2 interface","IFsiDirectoryItem2 interface [IMAPI]","AddTreeWithNamedStreams method","IFsiDirectoryItem2.AddTreeWithNamedStreams","IFsiDirectoryItem2::AddTreeWithNamedStreams","imapi.ifsidirectoryitem2_addtreewithnamedstreams","imapi2fs/IFsiDirectoryItem2::AddTreeWithNamedStreams"]
old-location: imapi\ifsidirectoryitem2_addtreewithnamedstreams.htm
tech.root: imapi
ms.assetid: d87d1932-85d4-4d7d-99a7-933a87b48b6a
ms.date: 12/05/2018
ms.keywords: AddTreeWithNamedStreams, AddTreeWithNamedStreams method [IMAPI], AddTreeWithNamedStreams method [IMAPI],IFsiDirectoryItem2 interface, IFsiDirectoryItem2 interface [IMAPI],AddTreeWithNamedStreams method, IFsiDirectoryItem2.AddTreeWithNamedStreams, IFsiDirectoryItem2::AddTreeWithNamedStreams, imapi.ifsidirectoryitem2_addtreewithnamedstreams, imapi2fs/IFsiDirectoryItem2::AddTreeWithNamedStreams
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsiDirectoryItem2::AddTreeWithNamedStreams
 - imapi2fs/IFsiDirectoryItem2::AddTreeWithNamedStreams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFsiDirectoryItem2.AddTreeWithNamedStreams
---

# IFsiDirectoryItem2::AddTreeWithNamedStreams


## -description

Adds the contents of a directory tree along with named streams associated with all files to the file system image.

## -parameters

### -param sourceDirectory [in]

String that contains the relative path of the directory tree to create. The path should contain only valid characters as per file system naming conventions. 
This parameter cannot be <b>NULL</b>. 

<div class="alert"><b>Note</b>  You must specify the full path when calling this method from the root directory item.</div>
<div> </div>

### -param includeBaseDirectory [in]

Set to <b>VARIANT_TRUE</b> to include the directory in <i>sourceDirectory</i> as a subdirectory in the file system image. Otherwise, <b>VARIANT_FALSE</b>.

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
Feature is not supported for the current file system revision, and as a result, will be created without this feature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
<dt>Value: 0xC0AAB101</dt>
</dl>
</td>
<td width="60%">
The value specified for parameter '<i>%1!ls!</i>' is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_NOT_IN_FILE_SYSTEM</b></dt>
<dt>Value: 0xC0AAB10B</dt>
</dl>
</td>
<td width="60%">
<i>ls!'</i> is not part of the file system. It must be added to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DATA_STREAM_CREATE_FAILURE</b></dt>
<dt>Value: Value: 0xC0AAB12AL</dt>
</dl>
</td>
<td width="60%">
Error occurred while creating data stream for <i>'%1!ls!'</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DATA_STREAM_READ_FAILURE</b></dt>
<dt>Value: 0xC0AAB129L</dt>
</dl>
</td>
<td width="60%">
Cannot read data from stream supplied for file <i>'%1!ls!'</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_READONLY</b></dt>
<dt>Value: 0xC0AAB102</dt>
</dl>
</td>
<td width="60%">
The referenced <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> object is in read only mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DUP_NAME</b></dt>
<dt>Value: 0xC0AAB112L</dt>
</dl>
</td>
<td width="60%">
<i>'%1!ls!'</i> name already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_IMAGE_SIZE_LIMIT</b></dt>
<dt>Value: 0xC0AAB120L</dt>
</dl>
</td>
<td width="60%">
Adding <i>'%1!ls!'</i> would result in a result image having a size larger than the current configured limit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DATA_STREAM_INCONSISTENCY</b></dt>
<dt>Value: 0xC0AAB128L</dt>
</dl>
</td>
<td width="60%">
The data stream supplied for the file <i>'%1!ls!'</i> is inconsistent; expected <i>%2!I64d!</i> bytes, found <i>%3!I64d!</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>Value: 0x8007000EL</dt>
</dl>
</td>
<td width="60%">
Failed to allocate required memory.

</td>
</tr>
</table>

## -remarks

The parent directory for the new sub-directory must already exist within the file system image.

The sub-directory structure within specified <i>sourceDirectory</i> is implicitly mirrored in the file system image. 
If file or directory collisions occur, the content of the specified source directory prevails. 

The file system image is overwritten with the appropriate directories and files from the source directory.
If an exception occurs during processing, the file system image reverts to its previous state.

If this method is invoked for a file system object that does not contain UDF in the list of file systems enabled for creation in the resultant image or if the UDF revision is below 2.00, this method returns success code <b>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</b>. This indicates that the named streams have been added but will not appear in the resultant file system image unless UDF revision 2.00 or higher is enabled in the file system object.


When utilizing alternate data streams (ADS) it is important to note that the file system image has a limitation of  1000 streams. Exceeding this number will result in lost data.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2">IFsiDirectoryItem2</a>