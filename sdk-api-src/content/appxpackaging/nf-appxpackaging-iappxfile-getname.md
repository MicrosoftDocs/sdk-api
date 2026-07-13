---
UID: NF:appxpackaging.IAppxFile.GetName
title: IAppxFile::GetName (appxpackaging.h)
description: Retrieves the name of the file, including its path relative to the package root directory.
helpviewer_keywords: ["GetName","GetName method [App packaging and management]","GetName method [App packaging and management]","IAppxFile interface","IAppxFile interface [App packaging and management]","GetName method","IAppxFile.GetName","IAppxFile::GetName","appxpackaging/IAppxFile::GetName","appxpkg.iappxfile_getname"]
old-location: appxpkg\iappxfile_getname.htm
tech.root: appxpkg
ms.assetid: B56F7A31-686A-4A8B-9388-E30718632AE9
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetName method, IAppxFile.GetName, IAppxFile::GetName, appxpackaging/IAppxFile::GetName, appxpkg.iappxfile_getname
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxFile::GetName
 - appxpackaging/IAppxFile::GetName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFile.GetName
---

# IAppxFile::GetName


## -description

Retrieves the name of the file, including its path relative to the package root directory.

## -parameters

### -param fileName [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

A string that contains the name and relative path of the file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The string returned in <i>fileName</i> is identical to the file name listed in the block map.

The caller is responsible for deallocating the memory used by <i>fileName</i>. Use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to deallocate the string's memory.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-extract-content-from-a-package">Quickstart: Extract app package contents</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>