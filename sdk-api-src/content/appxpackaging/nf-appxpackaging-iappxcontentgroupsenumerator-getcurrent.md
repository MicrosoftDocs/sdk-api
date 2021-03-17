---
UID: NF:appxpackaging.IAppxContentGroupsEnumerator.GetCurrent
title: IAppxContentGroupsEnumerator::GetCurrent (appxpackaging.h)
description: Gets the content group at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [App packaging and management]","GetCurrent method [App packaging and management]","IAppxContentGroupsEnumerator interface","IAppxContentGroupsEnumerator interface [App packaging and management]","GetCurrent method","IAppxContentGroupsEnumerator.GetCurrent","IAppxContentGroupsEnumerator::GetCurrent","appxpackaging/IAppxContentGroupsEnumerator::GetCurrent","appxpkg.iappxcontentgroupsenumerator_getcurrent"]
old-location: appxpkg\iappxcontentgroupsenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: 1A7055F5-6121-4A3A-AE7C-4BFDF6D7F1A9
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxContentGroupsEnumerator interface, IAppxContentGroupsEnumerator interface [App packaging and management],GetCurrent method, IAppxContentGroupsEnumerator.GetCurrent, IAppxContentGroupsEnumerator::GetCurrent, appxpackaging/IAppxContentGroupsEnumerator::GetCurrent, appxpkg.iappxcontentgroupsenumerator_getcurrent
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
 - IAppxContentGroupsEnumerator::GetCurrent
 - appxpackaging/IAppxContentGroupsEnumerator::GetCurrent
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
 - IAppxContentGroupsEnumerator.GetCurrent
---

# IAppxContentGroupsEnumerator::GetCurrent


## -description

Gets the content group at the current position of the enumerator.

## -parameters

### -param stream [out, retval]

The current content group.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has passed the last item in the collection.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupsenumerator">IAppxContentGroupsEnumerator</a>