---
UID: NF:appxpackaging.IAppxSourceContentGroupMapReader.GetRequiredGroup
title: IAppxSourceContentGroupMapReader::GetRequiredGroup (appxpackaging.h)
description: Gets the required content group from the source content group map.
helpviewer_keywords: ["GetRequiredGroup","GetRequiredGroup method [App packaging and management]","GetRequiredGroup method [App packaging and management]","IAppxSourceContentGroupMapReader interface","IAppxSourceContentGroupMapReader interface [App packaging and management]","GetRequiredGroup method","IAppxSourceContentGroupMapReader.GetRequiredGroup","IAppxSourceContentGroupMapReader::GetRequiredGroup","appxpackaging/IAppxSourceContentGroupMapReader::GetRequiredGroup","appxpkg.iappxsourcecontentgroupmapreader_getrequiredgroup"]
old-location: appxpkg\iappxsourcecontentgroupmapreader_getrequiredgroup.htm
tech.root: appxpkg
ms.assetid: 4C85F79F-CD91-4038-AF23-413E04CBA5AA
ms.date: 12/05/2018
ms.keywords: GetRequiredGroup, GetRequiredGroup method [App packaging and management], GetRequiredGroup method [App packaging and management],IAppxSourceContentGroupMapReader interface, IAppxSourceContentGroupMapReader interface [App packaging and management],GetRequiredGroup method, IAppxSourceContentGroupMapReader.GetRequiredGroup, IAppxSourceContentGroupMapReader::GetRequiredGroup, appxpackaging/IAppxSourceContentGroupMapReader::GetRequiredGroup, appxpkg.iappxsourcecontentgroupmapreader_getrequiredgroup
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
 - IAppxSourceContentGroupMapReader::GetRequiredGroup
 - appxpackaging/IAppxSourceContentGroupMapReader::GetRequiredGroup
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
 - IAppxSourceContentGroupMapReader.GetRequiredGroup
---

# IAppxSourceContentGroupMapReader::GetRequiredGroup


## -description

Gets the required content group from the source content group map.

## -parameters

### -param requiredGroup [out, retval]

The required content group.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxsourcecontentgroupmapreader">IAppxSourceContentGroupMapReader</a>