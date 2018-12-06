---
UID: NF:imapi2fs.IFileSystemImage.IdentifyFileSystemsOnDisc
title: IFileSystemImage::IdentifyFileSystemsOnDisc
author: windows-sdk-content
description: Retrieves a list of the different types of file systems on the optical media.
old-location: imapi\ifilesystemimage_identifyfilesystemsondisc.htm
tech.root: imapi
ms.assetid: 381be283-c877-44f0-9d96-b9e80a6aeec8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileSystemImage interface [IMAPI],IdentifyFileSystemsOnDisc method, IFileSystemImage.IdentifyFileSystemsOnDisc, IFileSystemImage::IdentifyFileSystemsOnDisc, IdentifyFileSystemsOnDisc, IdentifyFileSystemsOnDisc method [IMAPI], IdentifyFileSystemsOnDisc method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_identifyfilesystemsondisc, imapi2fs/IFileSystemImage::IdentifyFileSystemsOnDisc
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
 - IFileSystemImage.IdentifyFileSystemsOnDisc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage::IdentifyFileSystemsOnDisc


## -description


Retrieves a list of the different types of file systems on the optical media.


## -parameters




### -param discRecorder [in, optional]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface that identifies the recording device that contains the media. If this parameter is <b>NULL</b>, the <i>discRecorder</i>  specified in <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a> will be used.


### -param fileSystems [out]

One or more files systems on the disc. For possible values, see <a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a> enumeration type.


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



Client applications can call <a href="https://msdn.microsoft.com/bbac5b93-669f-45ea-9a3d-e2dd7f8bdcf6">IFileSystemImage::GetDefaultFileSystemForImport</a> with the value returned by this method to determine the type of file system to import.




## -see-also




<a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a>



<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>
 

 

