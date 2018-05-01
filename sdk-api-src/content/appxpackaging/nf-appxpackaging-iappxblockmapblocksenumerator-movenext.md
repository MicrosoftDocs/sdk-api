---
UID: NF:appxpackaging.IAppxBlockMapBlocksEnumerator.MoveNext
title: IAppxBlockMapBlocksEnumerator::MoveNext method
author: windows-driver-content
description: Advances the position of the enumerator to the next block.
old-location: appxpkg\iappxblockmapblocksenumerator_movenext.htm
old-project: appxpkg
ms.assetid: CDF8C336-CFF8-41FE-AC3E-48988209850E
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAppxBlockMapBlocksEnumerator, IAppxBlockMapBlocksEnumerator interface [App packaging and management], MoveNext method, IAppxBlockMapBlocksEnumerator::MoveNext, MoveNext method [App packaging and management], MoveNext method [App packaging and management], IAppxBlockMapBlocksEnumerator interface, MoveNext,IAppxBlockMapBlocksEnumerator.MoveNext, appxpackaging/IAppxBlockMapBlocksEnumerator::MoveNext, appxpkg.iappxblockmapblocksenumerator_movenext
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
-	IAppxBlockMapBlocksEnumerator.MoveNext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapBlocksEnumerator::MoveNext method


## -description


Advances the position of the enumerator to the next block.


## -parameters




### -param hasNext [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator successfully advances

<b>FALSE</b> if the enumerator has passed the end of the collection.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

Note that when the enumerator passes the end of the collection for the first time, <i>hasNext</i> = <b>FALSE</b>,  but the method succeeds and returns <b>S_OK</b>. However, the method returns <b>E_BOUNDS</b> if you subsequently call another MoveNext after you have already passed the end of the collection, and you have previously received  <i>hasNext</i> = <b>FALSE</b>.





## -see-also




<a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>
 

 

