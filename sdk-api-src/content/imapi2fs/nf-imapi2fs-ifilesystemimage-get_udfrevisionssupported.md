---
UID: NF:imapi2fs.IFileSystemImage.get_UDFRevisionsSupported
title: IFileSystemImage::get_UDFRevisionsSupported
author: windows-sdk-content
description: Retrieves a list of supported UDF revision levels.
old-location: imapi\ifilesystemimage_get_udfrevisionssupported.htm
tech.root: imapi
ms.assetid: ad9b4a68-5fef-4092-9cef-4b5ebd9c5093
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_UDFRevisionsSupported method, IFileSystemImage.get_UDFRevisionsSupported, IFileSystemImage::get_UDFRevisionsSupported, get_UDFRevisionsSupported, get_UDFRevisionsSupported method [IMAPI], get_UDFRevisionsSupported method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_udfrevisionssupported, imapi2fs/IFileSystemImage::get_UDFRevisionsSupported
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
 - IFileSystemImage.get_UDFRevisionsSupported
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
- IFileSystemImage.get_UDFRevisionsSupported
: 
---

# IFileSystemImage::get_UDFRevisionsSupported


## -description


Retrieves a list of supported UDF revision levels.


## -parameters




### -param pVal [out]

List of supported UDF revision levels. Each element of the list is VARIANT. The variant type is <b>VT_I4</b>. The <b>lVal</b> member of the variant contains the revision level.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



The value is encoded according to the UDF specification, except the variable size is LONG. For example, revision level 1.02 is represented as 0x102.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/c854a8db-730a-42a3-b50c-fb8fec271b57">IFileSystemImage::get_UDFRevision</a>



<a href="https://msdn.microsoft.com/a4b0e73b-6bef-44e1-b0b7-9a4e0fcc1370">IFileSystemImage::put_UDFRevision</a>
 

 

