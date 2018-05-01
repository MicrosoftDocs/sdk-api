---
UID: NF:appxpackaging.IAppxFilesEnumerator.GetHasCurrent
title: IAppxFilesEnumerator::GetHasCurrent method
author: windows-driver-content
description: Determines whether there is a payload file at the current position of the enumerator.
old-location: appxpkg\iappxfilesenumerator_gethascurrent.htm
old-project: appxpkg
ms.assetid: 4CC798E4-5FD2-45DE-BD3A-0B036601BEDB
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management], IAppxFilesEnumerator interface, GetHasCurrent,IAppxFilesEnumerator.GetHasCurrent, IAppxFilesEnumerator, IAppxFilesEnumerator interface [App packaging and management], GetHasCurrent method, IAppxFilesEnumerator::GetHasCurrent, appxpackaging/IAppxFilesEnumerator::GetHasCurrent, appxpkg.iappxfilesenumerator_gethascurrent
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
-	IAppxFilesEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFilesEnumerator::GetHasCurrent method


## -description


Determines whether there is a payload file at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the current position references a payload file; <b>FALSE</b> if the enumerator has passed the end of the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724">IAppxFilesEnumerator</a>
 

 

