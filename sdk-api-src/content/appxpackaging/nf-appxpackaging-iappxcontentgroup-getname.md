---
UID: NF:appxpackaging.IAppxContentGroup.GetName
title: IAppxContentGroup::GetName (appxpackaging.h)
description: Gets the name of the content group.
helpviewer_keywords: ["GetName","GetName method [App packaging and management]","GetName method [App packaging and management]","IAppxContentGroup interface","IAppxContentGroup interface [App packaging and management]","GetName method","IAppxContentGroup.GetName","IAppxContentGroup::GetName","appxpackaging/IAppxContentGroup::GetName","appxpkg.iappxcontentgroup_getname"]
old-location: appxpkg\iappxcontentgroup_getname.htm
tech.root: appxpkg
ms.assetid: 169E5A94-F7F7-4BFC-8E19-9E830C920E1B
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxContentGroup interface, IAppxContentGroup interface [App packaging and management],GetName method, IAppxContentGroup.GetName, IAppxContentGroup::GetName, appxpackaging/IAppxContentGroup::GetName, appxpkg.iappxcontentgroup_getname
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
 - IAppxContentGroup::GetName
 - appxpackaging/IAppxContentGroup::GetName
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
 - IAppxContentGroup.GetName
---

# IAppxContentGroup::GetName


## -description

Gets the name of the content group.

## -parameters

### -param groupName [out, retval]

The content group name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroup">IAppxContentGroup</a>