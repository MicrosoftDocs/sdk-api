---
UID: NF:appxpackaging.IAppxBlockMapFile.GetLocalFileHeaderSize
title: IAppxBlockMapFile::GetLocalFileHeaderSize
author: windows-sdk-content
description: Retrieves the size of the zip local file header of the associated zip file item.
old-location: appxpkg\iappxblockmapfile_getlocalfileheadersize.htm
old-project: appxpkg
ms.assetid: 2BBABACF-089B-4711-B384-627E921B044A
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetLocalFileHeaderSize, GetLocalFileHeaderSize method [App packaging and management], GetLocalFileHeaderSize method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetLocalFileHeaderSize method, IAppxBlockMapFile.GetLocalFileHeaderSize, IAppxBlockMapFile::GetLocalFileHeaderSize, appxpackaging/IAppxBlockMapFile::GetLocalFileHeaderSize, appxpkg.iappxblockmapfile_getlocalfileheadersize
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
-	IAppxBlockMapFile.GetLocalFileHeaderSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapFile::GetLocalFileHeaderSize


## -description


Retrieves the size of the zip local file header of the associated zip file item.


## -parameters




### -param lfhSize [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT32</a>*</b>

In a valid app package, <i>lfhSize</i> corresponds to the size of the zip local file header of the associated zip file item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>
 

 

