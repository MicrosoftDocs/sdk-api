---
UID: NF:appxpackaging.IAppxPackageReader.GetPayloadFiles
title: IAppxPackageReader::GetPayloadFiles (appxpackaging.h)
author: windows-sdk-content
description: Retrieves an enumerator that iterates through the payload files in the package.
old-location: appxpkg\iappxpackagereader_getpayloadfiles.htm
tech.root: appxpkg
ms.assetid: 20883A4E-BE7B-4312-978A-3BF9362CA6DA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPayloadFiles, GetPayloadFiles method [App packaging and management], GetPayloadFiles method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetPayloadFiles method, IAppxPackageReader.GetPayloadFiles, IAppxPackageReader::GetPayloadFiles, appxpackaging/IAppxPackageReader::GetPayloadFiles, appxpkg.iappxpackagereader_getpayloadfiles
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
 - IAppxPackageReader.GetPayloadFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxPackageReader::GetPayloadFiles


## -description


Retrieves an enumerator that iterates through the payload files in the package.


## -parameters




### -param filesEnumerator [out, retval]

Type: <b><a href="https://msdn.microsoft.com/A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724">IAppxFilesEnumerator</a>**</b>

 An enumerator over all payload files in the package. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>



<a href="https://msdn.microsoft.com/8CCF9135-308F-4BDC-A67F-1E3ED2ACF565">IAppxPackageReader::GetFootprintFile</a>



<a href="https://msdn.microsoft.com/83E6931D-405C-4A93-BE70-F505D484CB7F">IAppxPackageReader::GetPayloadFile</a>
 

 

