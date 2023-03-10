---
UID: NF:appxpackaging.IAppxContentGroupMapReader.GetRequiredGroup
title: IAppxContentGroupMapReader::GetRequiredGroup (appxpackaging.h)
description: Gets the required content group from the content group map.
helpviewer_keywords: ["GetRequiredGroup","GetRequiredGroup method [App packaging and management]","GetRequiredGroup method [App packaging and management]","IAppxContentGroupMapReader interface","IAppxContentGroupMapReader interface [App packaging and management]","GetRequiredGroup method","IAppxContentGroupMapReader.GetRequiredGroup","IAppxContentGroupMapReader::GetRequiredGroup","appxpackaging/IAppxContentGroupMapReader::GetRequiredGroup","appxpkg.iappxcontentgroupmapreader_getrequiredgroup"]
old-location: appxpkg\iappxcontentgroupmapreader_getrequiredgroup.htm
tech.root: appxpkg
ms.assetid: 45E4193E-EB4C-4D3D-989A-7AE35FDC2C77
ms.date: 12/05/2018
ms.keywords: GetRequiredGroup, GetRequiredGroup method [App packaging and management], GetRequiredGroup method [App packaging and management],IAppxContentGroupMapReader interface, IAppxContentGroupMapReader interface [App packaging and management],GetRequiredGroup method, IAppxContentGroupMapReader.GetRequiredGroup, IAppxContentGroupMapReader::GetRequiredGroup, appxpackaging/IAppxContentGroupMapReader::GetRequiredGroup, appxpkg.iappxcontentgroupmapreader_getrequiredgroup
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
 - IAppxContentGroupMapReader::GetRequiredGroup
 - appxpackaging/IAppxContentGroupMapReader::GetRequiredGroup
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
 - IAppxContentGroupMapReader.GetRequiredGroup
---

# IAppxContentGroupMapReader::GetRequiredGroup


## -description

Gets the required content group from the content group map.

## -parameters

### -param requiredGroup [out, retval]

The required content group.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupmapreader">IAppxContentGroupMapReader</a>