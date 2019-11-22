---
UID: NF:appxpackaging.IAppxBlockMapFile.GetLocalFileHeaderSize
title: IAppxBlockMapFile::GetLocalFileHeaderSize (appxpackaging.h)

description: Retrieves the size of the zip local file header of the associated zip file item.
old-location: appxpkg\iappxblockmapfile_getlocalfileheadersize.htm
tech.root: appxpkg
ms.assetid: 2BBABACF-089B-4711-B384-627E921B044A

ms.date: 12/05/2018
ms.keywords: GetLocalFileHeaderSize, GetLocalFileHeaderSize method [App packaging and management], GetLocalFileHeaderSize method [App packaging and management],IAppxBlockMapFile interface, IAppxBlockMapFile interface [App packaging and management],GetLocalFileHeaderSize method, IAppxBlockMapFile.GetLocalFileHeaderSize, IAppxBlockMapFile::GetLocalFileHeaderSize, appxpackaging/IAppxBlockMapFile::GetLocalFileHeaderSize, appxpkg.iappxblockmapfile_getlocalfileheadersize
ms.topic: method
f1_keywords: 
 - "appxpackaging/IAppxBlockMapFile.GetLocalFileHeaderSize"
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
 - IAppxBlockMapFile.GetLocalFileHeaderSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapFile::GetLocalFileHeaderSize


## -description


Retrieves the size of the zip local file header of the associated zip file item.


## -parameters




### -param lfhSize [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT32</a>*</b>

In a valid app package, <i>lfhSize</i> corresponds to the size of the zip local file header of the associated zip file item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>
 

 

