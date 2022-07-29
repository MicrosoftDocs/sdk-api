---
UID: NF:appxpackaging.IAppxContentGroupFilesEnumerator.GetHasCurrent
title: IAppxContentGroupFilesEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there is a file at the current position of the enumerator. (IAppxContentGroupFilesEnumerator.GetHasCurrent)
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxContentGroupFilesEnumerator interface","IAppxContentGroupFilesEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxContentGroupFilesEnumerator.GetHasCurrent","IAppxContentGroupFilesEnumerator::GetHasCurrent","appxpackaging/IAppxContentGroupFilesEnumerator::GetHasCurrent","appxpkg.iappxcontentgroupfilesenumerator__gethascurrent"]
old-location: appxpkg\iappxcontentgroupfilesenumerator__gethascurrent.htm
tech.root: appxpkg
ms.assetid: 3F058122-35E9-4CEF-96B0-1597CC106FB2
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxContentGroupFilesEnumerator interface, IAppxContentGroupFilesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxContentGroupFilesEnumerator.GetHasCurrent, IAppxContentGroupFilesEnumerator::GetHasCurrent, appxpackaging/IAppxContentGroupFilesEnumerator::GetHasCurrent, appxpkg.iappxcontentgroupfilesenumerator__gethascurrent
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
 - IAppxContentGroupFilesEnumerator::GetHasCurrent
 - appxpackaging/IAppxContentGroupFilesEnumerator::GetHasCurrent
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
 - IAppxContentGroupFilesEnumerator.GetHasCurrent
---

# IAppxContentGroupFilesEnumerator::GetHasCurrent


## -description

Determines whether there is a file at the current position of the enumerator.

## -parameters

### -param hasCurrent [out, retval]

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/appxpackaging/nn-appxpackaging-iappxcontentgroupfilesenumerator">IAppxContentGroupFilesEnumerator</a>

