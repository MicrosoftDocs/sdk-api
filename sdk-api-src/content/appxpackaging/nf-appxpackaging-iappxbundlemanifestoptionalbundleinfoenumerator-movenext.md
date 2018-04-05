---
UID: NF:appxpackaging.IAppxBundleManifestOptionalBundleInfoEnumerator.MoveNext
title: IAppxBundleManifestOptionalBundleInfoEnumerator::MoveNext method
author: windows-driver-content
description: Advances the position of the enumerator to the next set of optional bundle information.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfoenumerator_movenext.htm
old-project: appxpkg
ms.assetid: 4A157CF1-8254-47FF-886A-77C15BDCDA76
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: IAppxBundleManifestOptionalBundleInfoEnumerator, IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management], MoveNext method, IAppxBundleManifestOptionalBundleInfoEnumerator::MoveNext, MoveNext method [App packaging and management], MoveNext method [App packaging and management], IAppxBundleManifestOptionalBundleInfoEnumerator interface, MoveNext,IAppxBundleManifestOptionalBundleInfoEnumerator.MoveNext, appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator::MoveNext, appxpkg.iappxbundlemanifestoptionalbundleinfoenumerator_movenext
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
-	IAppxBundleManifestOptionalBundleInfoEnumerator.MoveNext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestOptionalBundleInfoEnumerator::MoveNext method


## -description


Advances the position of the enumerator to the next set of optional bundle information.


## -parameters




### -param hasNext [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator successfully advances

<b>FALSE</b> if the enumerator has passed the end of the collection.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

<div class="alert"><b>Note</b>  When the enumerator passes the end of the collection for the first time, <i>hasNext</i> = <b>FALSE</b>,  but the method succeeds and returns <b>S_OK</b>. However, the method returns <b>E_BOUNDS</b> if you subsequently call another MoveNext after you have already passed the end of the collection, and you have previously received  <i>hasNext</i> = <b>FALSE</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5BF38EC7-7C04-455B-AFAA-CC2A78E54A4F">IAppxBundleManifestOptionalBundleInfoEnumerator</a>
 

 

