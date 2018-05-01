---
UID: NF:appxpackaging.IAppxSourceContentGroupMapReader.GetAutomaticGroups
title: IAppxSourceContentGroupMapReader::GetAutomaticGroups method
author: windows-driver-content
description: Gets the automatic content group(s) from the source content group map.
old-location: appxpkg\iappxsourcecontentgroupmapreader_getautomaticgroups.htm
old-project: appxpkg
ms.assetid: DA6D0BEB-75ED-49B8-82A8-0B7C53E5C3C9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetAutomaticGroups method [App packaging and management], GetAutomaticGroups method [App packaging and management], IAppxSourceContentGroupMapReader interface, GetAutomaticGroups,IAppxSourceContentGroupMapReader.GetAutomaticGroups, IAppxSourceContentGroupMapReader, IAppxSourceContentGroupMapReader interface [App packaging and management], GetAutomaticGroups method, IAppxSourceContentGroupMapReader::GetAutomaticGroups, appxpackaging/IAppxSourceContentGroupMapReader::GetAutomaticGroups, appxpkg.iappxsourcecontentgroupmapreader_getautomaticgroups
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxSourceContentGroupMapReader.GetAutomaticGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxSourceContentGroupMapReader::GetAutomaticGroups method


## -description


Gets the automatic content group(s) from the source content group map.


## -parameters




### -param automaticGroupsEnumerator [out, retval]

An enumerator for the automatic content group(s).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EA0DF7E6-C4EF-4A58-A13F-EB3789239084">IAppxSourceContentGroupMapReader</a>
 

 

