---
UID: NF:imapi2fs.IFileSystemImage.put_WorkingDirectory
title: IFileSystemImage::put_WorkingDirectory
author: windows-sdk-content
description: Sets the temporary directory in which stash files are built.
old-location: imapi\ifilesystemimage_put_workingdirectory.htm
old-project: imapi
ms.assetid: bfe37cfe-654d-4923-b667-e44be7ce4715
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_WorkingDirectory method, IFileSystemImage.put_WorkingDirectory, IFileSystemImage::put_WorkingDirectory, imapi.ifilesystemimage_put_workingdirectory, imapi2fs/IFileSystemImage::put_WorkingDirectory, put_WorkingDirectory, put_WorkingDirectory method [IMAPI], put_WorkingDirectory method [IMAPI],IFileSystemImage interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.put_WorkingDirectory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImage::put_WorkingDirectory


## -description


Sets the temporary directory in which stash files are built. 


## -parameters




### -param newVal [in]

String that contains the path to the temporary working directory. The default is the current temp directory.


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
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_WORKING_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
The working directory <i>%1!ls!</i> is not valid.

Value: 0xC0AAB140

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_WORKING_DIRECTORY_SPACE</b></dt>
</dl>
</td>
<td width="60%">
Cannot set working directory to <i>%1!ls!</i>. Space available is <i>%2!I64d!</i> bytes, approximately <i>%3!I64d!</i> bytes required. 

Value: 0xC0AAB141

</td>
</tr>
</table>
 




## -remarks



  
Stash files are the temporary files used to build the file-system image.

An exception results if the existing stash files cannot move to the new working directory. 

You cannot change the working directory if a result stream exists for the file-system image.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/89c4fd34-6651-4056-9939-201f404ea6ee">IFileSystemImage::get_WorkingDirectory</a>
 

 

