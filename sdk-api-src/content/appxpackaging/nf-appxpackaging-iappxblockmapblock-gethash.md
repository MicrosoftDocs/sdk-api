---
UID: NF:appxpackaging.IAppxBlockMapBlock.GetHash
title: IAppxBlockMapBlock::GetHash
author: windows-sdk-content
description: Retrieves the hash value of the block.
old-location: appxpkg\iappxblockmapblock_gethash.htm
old-project: appxpkg
ms.assetid: 9A8460C2-2BEE-4CEC-BAF4-779E6F58664D
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetHash, GetHash method [App packaging and management], GetHash method [App packaging and management],IAppxBlockMapBlock interface, IAppxBlockMapBlock interface [App packaging and management],GetHash method, IAppxBlockMapBlock.GetHash, IAppxBlockMapBlock::GetHash, appxpackaging/IAppxBlockMapBlock::GetHash, appxpkg.iappxblockmapblock_gethash
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
 - IAppxBlockMapBlock.GetHash
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapBlock::GetHash


## -description


Retrieves the hash value of the block.


## -parameters




### -param bufferSize [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT32</a>*</b>

The length of  <i>buffer</i>.


### -param buffer [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>**</b>

The byte sequence representing the hash value of the block.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>buffer</i> value corresponds to the <b>Hash</b> attribute of the <b>Block</b> element.

The caller is responsible for deallocating the memory used for <i>buffer</i>. Use the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to deallocate the memory.




## -see-also




<a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a>
 

 

