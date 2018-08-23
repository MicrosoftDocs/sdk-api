---
UID: NF:appxpackaging.IAppxFile.GetSize
title: IAppxFile::GetSize
author: windows-sdk-content
description: Retrieves the uncompressed size of the file.
old-location: appxpkg\iappxfile_getsize.htm
old-project: appxpkg
ms.assetid: 73353CE0-98F8-4A8C-A259-A07C125B9EE9
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: GetSize, GetSize method [App packaging and management], GetSize method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetSize method, IAppxFile.GetSize, IAppxFile::GetSize, appxpackaging/IAppxFile::GetSize, appxpkg.iappxfile_getsize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFile.GetSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFile::GetSize


## -description


Retrieves the uncompressed size of the file.


## -parameters




### -param size [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a>*</b>

The uncompressed size, in bytes.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>
 

 

