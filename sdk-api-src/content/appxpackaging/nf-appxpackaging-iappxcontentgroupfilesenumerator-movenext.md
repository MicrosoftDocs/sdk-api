---
UID: NF:appxpackaging.IAppxContentGroupFilesEnumerator.MoveNext
title: IAppxContentGroupFilesEnumerator::MoveNext (appxpackaging.h)
description: Advances the position of the enumerator to the next file. (IAppxContentGroupFilesEnumerator.MoveNext)
helpviewer_keywords: ["IAppxContentGroupFilesEnumerator interface [App packaging and management]","MoveNext method","IAppxContentGroupFilesEnumerator.MoveNext","IAppxContentGroupFilesEnumerator::MoveNext","MoveNext","MoveNext method [App packaging and management]","MoveNext method [App packaging and management]","IAppxContentGroupFilesEnumerator interface","appxpackaging/IAppxContentGroupFilesEnumerator::MoveNext","appxpkg.iappxcontentgroupfilesenumerator__movenext"]
old-location: appxpkg\iappxcontentgroupfilesenumerator__movenext.htm
tech.root: appxpkg
ms.assetid: 39E27BFE-2383-4AB1-B83E-79573D87AAD6
ms.date: 12/05/2018
ms.keywords: IAppxContentGroupFilesEnumerator interface [App packaging and management],MoveNext method, IAppxContentGroupFilesEnumerator.MoveNext, IAppxContentGroupFilesEnumerator::MoveNext, MoveNext, MoveNext method [App packaging and management], MoveNext method [App packaging and management],IAppxContentGroupFilesEnumerator interface, appxpackaging/IAppxContentGroupFilesEnumerator::MoveNext, appxpkg.iappxcontentgroupfilesenumerator__movenext
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxContentGroupFilesEnumerator::MoveNext
 - appxpackaging/IAppxContentGroupFilesEnumerator::MoveNext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxContentGroupFilesEnumerator.MoveNext
---

# IAppxContentGroupFilesEnumerator::MoveNext


## -description

Advances the position of the enumerator to the next file.

## -parameters

### -param hasNext [out, retval]

<b>TRUE</b> if the enumerator successfully advances

<b>FALSE</b> if the enumerator has passed the end of the collection.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

<div class="alert"><b>Note</b>  When the enumerator passes the end of the collection for the first time, <i>hasNext</i> = <b>FALSE</b>,  but the method succeeds and returns <b>S_OK</b>. However, the method returns <b>E_BOUNDS</b> if you subsequently call another MoveNext after you have already passed the end of the collection, and you have previously received  <i>hasNext</i> = <b>FALSE</b>.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/appxpackaging/nn-appxpackaging-iappxcontentgroupfilesenumerator">IAppxContentGroupFilesEnumerator</a>

