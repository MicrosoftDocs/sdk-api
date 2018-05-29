---
UID: NF:appxpackaging.IAppxManifestApplicationsEnumerator.MoveNext
title: IAppxManifestApplicationsEnumerator::MoveNext
author: windows-sdk-content
description: Advances the position of the enumerator to the next application.
old-location: appxpkg\iappxmanifestapplicationsenumerator_movenext.htm
old-project: appxpkg
ms.assetid: 4F6EB510-4227-460B-9E2D-C304F33A931E
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxManifestApplicationsEnumerator interface [App packaging and management],MoveNext method, IAppxManifestApplicationsEnumerator.MoveNext, IAppxManifestApplicationsEnumerator::MoveNext, MoveNext, MoveNext method [App packaging and management], MoveNext method [App packaging and management],IAppxManifestApplicationsEnumerator interface, appxpackaging/IAppxManifestApplicationsEnumerator::MoveNext, appxpkg.iappxmanifestapplicationsenumerator_movenext
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestApplicationsEnumerator.MoveNext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestApplicationsEnumerator::MoveNext


## -description


Advances the position of the enumerator to the next application.


## -parameters




### -param hasNext [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator successfully advances

<b>FALSE</b> if the enumerator has passed the end of the collection.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

Note that when the enumerator passes the end of the collection for the first time, <i>hasNext</i> = <b>FALSE</b>,  but the method succeeds and returns <b>S_OK</b>. However, the method returns <b>E_BOUNDS</b> if you subsequently call another <b>MoveNext</b> after you have already passed the end of the collection, and you have previously received  <i>hasNext</i> = <b>FALSE</b>.





## -see-also




<a href="https://msdn.microsoft.com/49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F">IAppxManifestApplicationsEnumerator</a>
 

 

