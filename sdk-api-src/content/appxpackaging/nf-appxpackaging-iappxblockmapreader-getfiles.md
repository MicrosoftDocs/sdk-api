---
UID: NF:appxpackaging.IAppxBlockMapReader.GetFiles
title: IAppxBlockMapReader::GetFiles
author: windows-sdk-content
description: Retrieves an enumerator for traversing the files listed in the block map.
old-location: appxpkg\iappxblockmapreader_getfiles.htm
tech.root: appxpkg
ms.assetid: 7E46C555-8C61-4F26-9732-07E0DEEAF66F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFiles, GetFiles method [App packaging and management], GetFiles method [App packaging and management],IAppxBlockMapReader interface, IAppxBlockMapReader interface [App packaging and management],GetFiles method, IAppxBlockMapReader.GetFiles, IAppxBlockMapReader::GetFiles, appxpackaging/IAppxBlockMapReader::GetFiles, appxpkg.iappxblockmapreader_getfiles
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
 - IAppxBlockMapReader.GetFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBlockMapReader::GetFiles


## -description


Retrieves an enumerator for traversing the files listed in the block map.


## -parameters




### -param enumerator [out, retval]

Type: <b><a href="https://msdn.microsoft.com/AC2E55C3-1EEF-4867-BECC-37F6269029D6">IAppxBlockMapFilesEnumerator</a>**</b>

The enumerator of all the files listed in the block map.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>
 

 

