---
UID: NF:appxpackaging.IAppxBlockMapFile.ValidateFileHash
title: IAppxBlockMapFile::ValidateFileHash (appxpackaging.h)
author: windows-sdk-content
description: Validates the content of a file against the hashes stored in the block elements for this block map file.
old-location: appxpkg\iappxblockmapfile_validatefilehash.htm
tech.root: appxpkg
ms.assetid: 286EF8FD-925E-4B36-AFAB-D0EC949F8705
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapFile interface [App packaging and management],ValidateFileHash method, IAppxBlockMapFile.ValidateFileHash, IAppxBlockMapFile::ValidateFileHash, ValidateFileHash, ValidateFileHash method [App packaging and management], ValidateFileHash method [App packaging and management],IAppxBlockMapFile interface, appxpackaging/IAppxBlockMapFile::ValidateFileHash, appxpkg.iappxblockmapfile_validatefilehash
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBlockMapFile.ValidateFileHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapFile::ValidateFileHash


## -description


Validates the content of a file against the hashes stored in the block elements for this block map file.


## -parameters




### -param fileStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream that contains the file's contents. The stream must support <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">Read</a>, <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.


### -param isValid [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the file hash validates; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>
 

 

