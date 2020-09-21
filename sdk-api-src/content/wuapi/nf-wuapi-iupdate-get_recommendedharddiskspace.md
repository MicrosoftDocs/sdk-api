---
UID: NF:wuapi.IUpdate.get_RecommendedHardDiskSpace
title: IUpdate::get_RecommendedHardDiskSpace (wuapi.h)
description: Gets the recommended free space that should be available on the hard disk before you install the update. The free space is specified in megabytes (MB).
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","RecommendedHardDiskSpace property","IUpdate.RecommendedHardDiskSpace","IUpdate.get_RecommendedHardDiskSpace","IUpdate::RecommendedHardDiskSpace","IUpdate::get_RecommendedHardDiskSpace","RecommendedHardDiskSpace property [Windows Update Agent]","RecommendedHardDiskSpace property [Windows Update Agent]","IUpdate interface","get_RecommendedHardDiskSpace","wua.iupdate_recommendedharddiskspace","wuapi/IUpdate::RecommendedHardDiskSpace","wuapi/IUpdate::get_RecommendedHardDiskSpace"]
old-location: wua\iupdate_recommendedharddiskspace.htm
tech.root: wua
ms.assetid: 958d3de3-b2e0-47e0-9a71-b12ff6669242
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],RecommendedHardDiskSpace property, IUpdate.RecommendedHardDiskSpace, IUpdate.get_RecommendedHardDiskSpace, IUpdate::RecommendedHardDiskSpace, IUpdate::get_RecommendedHardDiskSpace, RecommendedHardDiskSpace property [Windows Update Agent], RecommendedHardDiskSpace property [Windows Update Agent],IUpdate interface, get_RecommendedHardDiskSpace, wua.iupdate_recommendedharddiskspace, wuapi/IUpdate::RecommendedHardDiskSpace, wuapi/IUpdate::get_RecommendedHardDiskSpace
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_RecommendedHardDiskSpace
 - wuapi/IUpdate::get_RecommendedHardDiskSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.RecommendedHardDiskSpace
 - IUpdate.get_RecommendedHardDiskSpace
---

# IUpdate::get_RecommendedHardDiskSpace


## -description

Gets the recommended free space that should be available on the hard disk before you install the update. The free space is specified in megabytes (MB).

This property is read-only.

## -parameters

## -remarks

The following properties of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface return 0 (zero) when the information is not available:

<ul>
<li>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed">RecommendedCpuSpeed</a>
</li>
<li><b>RecommendedHardDiskSpace</b></li>
<li>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedmemory">RecommendedMemory</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>