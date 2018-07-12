---
UID: NF:appxpackaging.IAppxBlockMapFile.GetName
title: IAppxBlockMapFile::GetName
author: windows-sdk-content
description: Retrieves the name of the associated zip file item.
old-location: appxpkg\iappxblockmapfile_getname.htm
old-project: appxpkg
ms.assetid: 82D100DB-CAE8-4FF7-B428-B14E8CBDE7A5
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetName method, IAppxBlockMapFile.GetName, IAppxBlockMapFile::GetName, appxpackaging/IAppxBlockMapFile::GetName, appxpkg.iappxblockmapfile_getname
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
 - IAppxBlockMapFile.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapFile::GetName


## -description


Retrieves the name of the associated zip file item.


## -parameters




### -param name [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

In a valid app package, <i>name</i> corresponds to the name of the associated zip file item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller is responsible for deallocating the memory used for <i>name</i>. Use the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to deallocate the memory.




## -see-also




<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>
 

 

