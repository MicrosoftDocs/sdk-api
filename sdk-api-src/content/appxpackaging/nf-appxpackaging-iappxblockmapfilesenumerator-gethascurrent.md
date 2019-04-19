---
UID: NF:appxpackaging.IAppxBlockMapFilesEnumerator.GetHasCurrent
title: IAppxBlockMapFilesEnumerator::GetHasCurrent (appxpackaging.h)
author: windows-sdk-content
description: Determines whether there is a file at the current position of the enumerator.
old-location: appxpkg\iappxblockmapfilesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: B0021CBC-9A3F-4D2D-8898-FE797396B312
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxBlockMapFilesEnumerator interface, IAppxBlockMapFilesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxBlockMapFilesEnumerator.GetHasCurrent, IAppxBlockMapFilesEnumerator::GetHasCurrent, appxpackaging/IAppxBlockMapFilesEnumerator::GetHasCurrent, appxpkg.iappxblockmapfilesenumerator_gethascurrent
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
 - IAppxBlockMapFilesEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapFilesEnumerator::GetHasCurrent


## -description


Determines whether there is a file at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/AC2E55C3-1EEF-4867-BECC-37F6269029D6">IAppxBlockMapFilesEnumerator</a>
 

 

