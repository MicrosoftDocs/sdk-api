---
UID: NF:appxpackaging.IAppxBlockMapBlocksEnumerator.GetHasCurrent
title: IAppxBlockMapBlocksEnumerator::GetHasCurrent method
author: windows-driver-content
description: Determines whether there is a block at the current position of the enumerator.
old-location: appxpkg\iappxblockmapblocksenumerator_gethascurrent.htm
old-project: appxpkg
ms.assetid: AC12BCDD-201C-4F22-B39E-1349EB84ED00
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management], IAppxBlockMapBlocksEnumerator interface, GetHasCurrent,IAppxBlockMapBlocksEnumerator.GetHasCurrent, IAppxBlockMapBlocksEnumerator, IAppxBlockMapBlocksEnumerator interface [App packaging and management], GetHasCurrent method, IAppxBlockMapBlocksEnumerator::GetHasCurrent, appxpackaging/IAppxBlockMapBlocksEnumerator::GetHasCurrent, appxpkg.iappxblockmapblocksenumerator_gethascurrent
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
-	IAppxBlockMapBlocksEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapBlocksEnumerator::GetHasCurrent method


## -description


Determines whether there is a block at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>
 

 

