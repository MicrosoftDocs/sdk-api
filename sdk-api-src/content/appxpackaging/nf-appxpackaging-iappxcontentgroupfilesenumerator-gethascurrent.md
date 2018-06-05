---
UID: NF:appxpackaging.IAppxContentGroupFilesEnumerator.GetHasCurrent
title: IAppxContentGroupFilesEnumerator::GetHasCurrent
author: windows-sdk-content
description: Determines whether there is a file at the current position of the enumerator.
old-location: appxpkg\iappxcontentgroupfilesenumerator__gethascurrent.htm
old-project: appxpkg
ms.assetid: 3F058122-35E9-4CEF-96B0-1597CC106FB2
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxContentGroupFilesEnumerator interface, IAppxContentGroupFilesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxContentGroupFilesEnumerator.GetHasCurrent, IAppxContentGroupFilesEnumerator::GetHasCurrent, appxpackaging/IAppxContentGroupFilesEnumerator::GetHasCurrent, appxpkg.iappxcontentgroupfilesenumerator__gethascurrent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxContentGroupFilesEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxContentGroupFilesEnumerator::GetHasCurrent


## -description


Determines whether there is a file at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B831A43B-9062-4763-8702-B487E57FD0C2">IAppxContentGroupFilesEnumerator</a>
 

 

