---
UID: NF:appxpackaging.IAppxContentGroupMapReader.GetAutomaticGroups
title: IAppxContentGroupMapReader::GetAutomaticGroups method
author: windows-driver-content
description: Gets the automatic content group(s) from the content group map.
old-location: appxpkg\iappxcontentgroupmapreader_getautomaticgroups.htm
old-project: appxpkg
ms.assetid: 3A5FE3A2-8D0D-4073-94FE-B0AC5DBF2D25
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetAutomaticGroups method [App packaging and management], GetAutomaticGroups method [App packaging and management], IAppxContentGroupMapReader interface, GetAutomaticGroups,IAppxContentGroupMapReader.GetAutomaticGroups, IAppxContentGroupMapReader, IAppxContentGroupMapReader interface [App packaging and management], GetAutomaticGroups method, IAppxContentGroupMapReader::GetAutomaticGroups, appxpackaging/IAppxContentGroupMapReader::GetAutomaticGroups, appxpkg.iappxcontentgroupmapreader_getautomaticgroups
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxContentGroupMapReader.GetAutomaticGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxContentGroupMapReader::GetAutomaticGroups method


## -description


Gets the automatic content group(s) from the content group map.


## -parameters




### -param automaticGroupsEnumerator [out, retval]

An enumerator for the automatic content group(s).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/45C6F61E-8CF6-4188-9715-3954562F8AB0">IAppxContentGroupMapReader</a>
 

 

