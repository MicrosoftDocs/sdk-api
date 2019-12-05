---
UID: NF:appxpackaging.IAppxBlockMapFile.GetName
title: IAppxBlockMapFile::GetName (appxpackaging.h)
description: Retrieves the name of the associated zip file item.
old-location: appxpkg\iappxblockmapfile_getname.htm
tech.root: appxpkg
ms.assetid: 82D100DB-CAE8-4FF7-B428-B14E8CBDE7A5
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetName method, IAppxBlockMapFile.GetName, IAppxBlockMapFile::GetName, appxpackaging/IAppxBlockMapFile::GetName, appxpkg.iappxblockmapfile_getname
ms.topic: method
f1_keywords:
- appxpackaging/IAppxBlockMapFile.GetName
dev_langs:
- c++
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
- IAppxBlockMapFile.GetName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapFile::GetName


## -description


Retrieves the name of the associated zip file item.


## -parameters




### -param name [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

In a valid app package, <i>name</i> corresponds to the name of the associated zip file item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller is responsible for deallocating the memory used for <i>name</i>. Use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to deallocate the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>
 

 

