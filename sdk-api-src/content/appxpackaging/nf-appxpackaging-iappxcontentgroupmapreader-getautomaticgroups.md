---
UID: NF:appxpackaging.IAppxContentGroupMapReader.GetAutomaticGroups
title: IAppxContentGroupMapReader::GetAutomaticGroups (appxpackaging.h)
description: Gets the automatic content group(s) from the content group map.
helpviewer_keywords: ["GetAutomaticGroups","GetAutomaticGroups method [App packaging and management]","GetAutomaticGroups method [App packaging and management]","IAppxContentGroupMapReader interface","IAppxContentGroupMapReader interface [App packaging and management]","GetAutomaticGroups method","IAppxContentGroupMapReader.GetAutomaticGroups","IAppxContentGroupMapReader::GetAutomaticGroups","appxpackaging/IAppxContentGroupMapReader::GetAutomaticGroups","appxpkg.iappxcontentgroupmapreader_getautomaticgroups"]
old-location: appxpkg\iappxcontentgroupmapreader_getautomaticgroups.htm
tech.root: appxpkg
ms.assetid: 3A5FE3A2-8D0D-4073-94FE-B0AC5DBF2D25
ms.date: 12/05/2018
ms.keywords: GetAutomaticGroups, GetAutomaticGroups method [App packaging and management], GetAutomaticGroups method [App packaging and management],IAppxContentGroupMapReader interface, IAppxContentGroupMapReader interface [App packaging and management],GetAutomaticGroups method, IAppxContentGroupMapReader.GetAutomaticGroups, IAppxContentGroupMapReader::GetAutomaticGroups, appxpackaging/IAppxContentGroupMapReader::GetAutomaticGroups, appxpkg.iappxcontentgroupmapreader_getautomaticgroups
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
 - IAppxContentGroupMapReader::GetAutomaticGroups
 - appxpackaging/IAppxContentGroupMapReader::GetAutomaticGroups
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
 - IAppxContentGroupMapReader.GetAutomaticGroups
---

# IAppxContentGroupMapReader::GetAutomaticGroups


## -description

Gets the automatic content group(s) from the content group map.

## -parameters

### -param automaticGroupsEnumerator [out, retval]

An enumerator for the automatic content group(s).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupmapreader">IAppxContentGroupMapReader</a>