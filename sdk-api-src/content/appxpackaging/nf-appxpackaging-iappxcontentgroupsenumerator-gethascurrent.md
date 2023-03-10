---
UID: NF:appxpackaging.IAppxContentGroupsEnumerator.GetHasCurrent
title: IAppxContentGroupsEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there is a content group at the current position of the enumerator.
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxContentGroupsEnumerator interface","IAppxContentGroupsEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxContentGroupsEnumerator.GetHasCurrent","IAppxContentGroupsEnumerator::GetHasCurrent","appxpackaging/IAppxContentGroupsEnumerator::GetHasCurrent","appxpkg.iappxcontentgroupsenumerator_gethascurrent"]
old-location: appxpkg\iappxcontentgroupsenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: 5935EA6A-AD7F-4462-B539-A01439D0A373
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxContentGroupsEnumerator interface, IAppxContentGroupsEnumerator interface [App packaging and management],GetHasCurrent method, IAppxContentGroupsEnumerator.GetHasCurrent, IAppxContentGroupsEnumerator::GetHasCurrent, appxpackaging/IAppxContentGroupsEnumerator::GetHasCurrent, appxpkg.iappxcontentgroupsenumerator_gethascurrent
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
 - IAppxContentGroupsEnumerator::GetHasCurrent
 - appxpackaging/IAppxContentGroupsEnumerator::GetHasCurrent
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
 - IAppxContentGroupsEnumerator.GetHasCurrent
---

# IAppxContentGroupsEnumerator::GetHasCurrent


## -description

Determines whether there is a content group at the current position of the enumerator.

## -parameters

### -param hasCurrent [out, retval]

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupsenumerator">IAppxContentGroupsEnumerator</a>