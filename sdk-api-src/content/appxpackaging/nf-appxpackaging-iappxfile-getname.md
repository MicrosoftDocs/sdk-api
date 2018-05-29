---
UID: NF:appxpackaging.IAppxFile.GetName
title: IAppxFile::GetName
author: windows-sdk-content
description: Retrieves the name of the file, including its path relative to the package root directory.
old-location: appxpkg\iappxfile_getname.htm
old-project: appxpkg
ms.assetid: B56F7A31-686A-4A8B-9388-E30718632AE9
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetName method, IAppxFile.GetName, IAppxFile::GetName, appxpackaging/IAppxFile::GetName, appxpkg.iappxfile_getname
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
-	IAppxFile.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFile::GetName


## -description


Retrieves the name of the file, including its path relative to the package root directory.


## -parameters




### -param fileName [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

A string that contains the name and relative path of the file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string returned in <i>fileName</i> is identical to the file name listed in the block map.

The caller is responsible for deallocating the memory used by <i>fileName</i>. Use the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to deallocate the string's memory.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/72C368F9-2EBA-4930-81CF-9B85717CC0AA">Quickstart: Extract app package contents</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>
 

 

