---
UID: NF:appxpackaging.IAppxContentGroupFilesEnumerator.GetCurrent
title: IAppxContentGroupFilesEnumerator::GetCurrent method
author: windows-driver-content
description: Gets the file from the content group at the current position of the enumerator.
old-location: appxpkg\iappxcontentgroupfilesenumerator__getcurrent.htm
old-project: appxpkg
ms.assetid: B8BD3A9A-5330-4328-9FFD-69BF07CA93C7
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetCurrent method [App packaging and management], GetCurrent method [App packaging and management], IAppxContentGroupFilesEnumerator interface, GetCurrent,IAppxContentGroupFilesEnumerator.GetCurrent, IAppxContentGroupFilesEnumerator, IAppxContentGroupFilesEnumerator interface [App packaging and management], GetCurrent method, IAppxContentGroupFilesEnumerator::GetCurrent, appxpackaging/IAppxContentGroupFilesEnumerator::GetCurrent, appxpkg.iappxcontentgroupfilesenumerator__getcurrent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxContentGroupFilesEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxContentGroupFilesEnumerator::GetCurrent method


## -description


Gets the file from the content group at the current position of the enumerator.


## -parameters




### -param file [out, retval]

The file at the position of the enumerator.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B831A43B-9062-4763-8702-B487E57FD0C2">IAppxContentGroupFilesEnumerator</a>
 

 

