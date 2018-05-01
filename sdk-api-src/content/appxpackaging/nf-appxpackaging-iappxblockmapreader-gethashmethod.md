---
UID: NF:appxpackaging.IAppxBlockMapReader.GetHashMethod
title: IAppxBlockMapReader::GetHashMethod method
author: windows-driver-content
description: Retrieves the URI for the hash algorithm used to create block hashes in the block map.
old-location: appxpkg\iappxblockmapreader_gethashmethod.htm
old-project: appxpkg
ms.assetid: 661E4F12-E426-4811-81FA-4F065C6E488A
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetHashMethod method [App packaging and management], GetHashMethod method [App packaging and management], IAppxBlockMapReader interface, GetHashMethod,IAppxBlockMapReader.GetHashMethod, IAppxBlockMapReader, IAppxBlockMapReader interface [App packaging and management], GetHashMethod method, IAppxBlockMapReader::GetHashMethod, appxpackaging/IAppxBlockMapReader::GetHashMethod, appxpkg.iappxblockmapreader_gethashmethod
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBlockMapReader.GetHashMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapReader::GetHashMethod method


## -description


Retrieves the URI for the hash algorithm used to create block hashes in the block map.


## -parameters




### -param hashMethod [out, retval]

Type: <b><a href="https://msdn.microsoft.com/a9e3688b-d64c-4396-9943-775971d2e739">IUri</a>**</b>

The hash algorithm used in this block map.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>hashMethod</i> value corresponds to the <b>HashMethod</b> attribute of the <a href="https://msdn.microsoft.com/75eed334-6c80-4eb3-8776-fc34d7aa5357">BlockMap</a> root element. 

<b>GetHashMethod</b> returns supported URIs for <a href="https://msdn.microsoft.com/de7b02d8-8d72-4e94-887f-5f319784e79b">DigestMethod</a>s.




## -see-also




<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>
 

 

