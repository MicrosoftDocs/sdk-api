---
UID: NF:appxpackaging.IAppxBlockMapFile.ValidateFileHash
title: IAppxBlockMapFile::ValidateFileHash
author: windows-sdk-content
description: Validates the content of a file against the hashes stored in the block elements for this block map file.
old-location: appxpkg\iappxblockmapfile_validatefilehash.htm
old-project: appxpkg
ms.assetid: 286EF8FD-925E-4B36-AFAB-D0EC949F8705
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxBlockMapFile interface [App packaging and management],ValidateFileHash method, IAppxBlockMapFile.ValidateFileHash, IAppxBlockMapFile::ValidateFileHash, ValidateFileHash, ValidateFileHash method [App packaging and management], ValidateFileHash method [App packaging and management],IAppxBlockMapFile interface, appxpackaging/IAppxBlockMapFile::ValidateFileHash, appxpkg.iappxblockmapfile_validatefilehash
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBlockMapFile.ValidateFileHash
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapFile::ValidateFileHash


## -description


Validates the content of a file against the hashes stored in the block elements for this block map file.


## -parameters




### -param fileStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream that contains the file's contents. The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.


### -param isValid [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the file hash validates; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>
 

 

