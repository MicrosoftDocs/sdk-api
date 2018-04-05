---
UID: NF:appxpackaging.IAppxFile.GetContentType
title: IAppxFile::GetContentType method
author: windows-driver-content
description: Retrieves the content type of the file.
old-location: appxpkg\iappxfile_getcontenttype.htm
old-project: appxpkg
ms.assetid: 86EE47E1-B2AD-4610-8C9A-679536F9C51D
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetContentType method [App packaging and management], GetContentType method [App packaging and management], IAppxFile interface, GetContentType,IAppxFile.GetContentType, IAppxFile, IAppxFile interface [App packaging and management], GetContentType method, IAppxFile::GetContentType, appxpackaging/IAppxFile::GetContentType, appxpkg.iappxfile_getcontenttype
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxFile.GetContentType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFile::GetContentType method


## -description


Retrieves the content type of the file.


## -parameters




### -param contentType [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The content type of the file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller is responsible for deallocating the memory used by <i>contentType</i>. Use the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to deallocate the string's memory.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/72C368F9-2EBA-4930-81CF-9B85717CC0AA">Quickstart: Extract app package contents</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>
 

 

