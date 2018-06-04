---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFsiFileItem2::AddStream


## -description


Associates a named stream with a specific file in the file system image.


## -parameters




### -param name [in]

A string represents the name of the named stream. This should not include the path and should only contain valid characters as per file system naming conventions.


### -param streamData [in]

An <b>IStream</b> interface of the named stream used to write to the resultant file system image.


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
<dt><b>E_POINTER</b></dt>
<dt>Value: 0x80004003</dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

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
<dt><b>IMAPI_E_READONLY</b></dt>
<dt>Value: 0xC0AAB102</dt>
</dl>
</td>
<td width="60%">
The referenced <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a> object is in read only mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_FSI_INTERNAL_ERROR</b></dt>
<dt>Value: 0xC0AAB100L</dt>
</dl>
</td>
<td width="60%">
Internal file system error has occurred.

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



The file to which the named stream will be added must already exist within the file system image. If this method is called with a <i>name</i> that already exists for a named stream, it will return an error and will not replace the existing named stream.


 


If this method is invoked for a file system object that does not contain UDF in the list of file systems enabled for creation in the resultant image or if the UDF revision is below 2.00, this method returns success code <b>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</b>. This success code indicates that the named stream has been added but will not appear in the resultant file system image unless UDF revision 2.00 or higher is enabled in the file system object.

Currently, <b>IMAPI_E_READONLY</b> is returned when this method is called on an imported file system image, regardless of the read only status of the image.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/f35d1cd9-8a04-4c12-9af3-38f2c44b8c06">IFsiFileItem2</a>
 

 

