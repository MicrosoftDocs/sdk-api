---
UID: NF:appxpackaging.IAppxContentGroup.GetFiles
title: IAppxContentGroup::GetFiles (appxpackaging.h)
description: Gets files from a content group.
helpviewer_keywords: ["GetFiles","GetFiles method [App packaging and management]","GetFiles method [App packaging and management]","IAppxContentGroup interface","IAppxContentGroup interface [App packaging and management]","GetFiles method","IAppxContentGroup.GetFiles","IAppxContentGroup::GetFiles","appxpackaging/IAppxContentGroup::GetFiles","appxpkg.iappxcontentgroup_getfiles"]
old-location: appxpkg\iappxcontentgroup_getfiles.htm
tech.root: appxpkg
ms.assetid: AC946014-C0A2-45F8-9287-5852FD1B9981
ms.date: 12/05/2018
ms.keywords: GetFiles, GetFiles method [App packaging and management], GetFiles method [App packaging and management],IAppxContentGroup interface, IAppxContentGroup interface [App packaging and management],GetFiles method, IAppxContentGroup.GetFiles, IAppxContentGroup::GetFiles, appxpackaging/IAppxContentGroup::GetFiles, appxpkg.iappxcontentgroup_getfiles
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
 - IAppxContentGroup::GetFiles
 - appxpackaging/IAppxContentGroup::GetFiles
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
 - IAppxContentGroup.GetFiles
---

# IAppxContentGroup::GetFiles


## -description

Gets files from a content group.

## -parameters

### -param enumerator [out, retval]

An enumerator for getting content group files.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroup">IAppxContentGroup</a>