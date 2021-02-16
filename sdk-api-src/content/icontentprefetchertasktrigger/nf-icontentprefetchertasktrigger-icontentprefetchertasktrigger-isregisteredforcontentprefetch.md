---
UID: NF:icontentprefetchertasktrigger.IContentPrefetcherTaskTrigger.IsRegisteredForContentPrefetch
title: IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch (icontentprefetchertasktrigger.h)
description: Indicates if an app package has registered for the content prefetch background task.
helpviewer_keywords: ["IContentPrefetcherTaskTrigger interface [Web Services for Windows]","IsRegisteredForContentPrefetch method","IContentPrefetcherTaskTrigger.IsRegisteredForContentPrefetch","IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch","IsRegisteredForContentPrefetch","IsRegisteredForContentPrefetch method [Web Services for Windows]","IsRegisteredForContentPrefetch method [Web Services for Windows]","IContentPrefetcherTaskTrigger interface","icontentprefetchertasktrigger/IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch","wsw.icontentprefetchertasktrigger_isregisteredforcontentprefetch"]
old-location: wsw\icontentprefetchertasktrigger_isregisteredforcontentprefetch.htm
tech.root: wsw
ms.assetid: 6F8A0A9B-CF05-47F9-8486-10DFE720E0DD
ms.date: 12/05/2018
ms.keywords: IContentPrefetcherTaskTrigger interface [Web Services for Windows],IsRegisteredForContentPrefetch method, IContentPrefetcherTaskTrigger.IsRegisteredForContentPrefetch, IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch, IsRegisteredForContentPrefetch, IsRegisteredForContentPrefetch method [Web Services for Windows], IsRegisteredForContentPrefetch method [Web Services for Windows],IContentPrefetcherTaskTrigger interface, icontentprefetchertasktrigger/IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch, wsw.icontentprefetchertasktrigger_isregisteredforcontentprefetch
req.header: icontentprefetchertasktrigger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch
 - icontentprefetchertasktrigger/IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IContentPrefetcherTaskTrigger.h
api_name:
 - IContentPrefetcherTaskTrigger.IsRegisteredForContentPrefetch
---

# IContentPrefetcherTaskTrigger::IsRegisteredForContentPrefetch


## -description

Indicates if an app package has registered for the content prefetch background task.

## -parameters

### -param packageFullName [in]

The package ID.

### -param isRegistered [out]

True if the app package has registered for the content prefetch background task; otherwise, false.

## -returns

Returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The method call was not made at the required Medium Integrity Level (Medium IL).


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/icontentprefetchertasktrigger/nn-icontentprefetchertasktrigger-icontentprefetchertasktrigger">IContentPrefetcherTaskTrigger</a>