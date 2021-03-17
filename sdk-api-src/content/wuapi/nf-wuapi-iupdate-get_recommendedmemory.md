---
UID: NF:wuapi.IUpdate.get_RecommendedMemory
title: IUpdate::get_RecommendedMemory (wuapi.h)
description: Gets the recommended physical memory size that should be available in your computer before you install the update. The physical memory size is specified in megabytes (MB).
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","RecommendedMemory property","IUpdate.RecommendedMemory","IUpdate.get_RecommendedMemory","IUpdate::RecommendedMemory","IUpdate::get_RecommendedMemory","RecommendedMemory property [Windows Update Agent]","RecommendedMemory property [Windows Update Agent]","IUpdate interface","get_RecommendedMemory","wua.iupdate_recommendedmemory","wuapi/IUpdate::RecommendedMemory","wuapi/IUpdate::get_RecommendedMemory"]
old-location: wua\iupdate_recommendedmemory.htm
tech.root: wua
ms.assetid: 68a8341b-ba0a-4694-89c3-34fefb950bf7
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],RecommendedMemory property, IUpdate.RecommendedMemory, IUpdate.get_RecommendedMemory, IUpdate::RecommendedMemory, IUpdate::get_RecommendedMemory, RecommendedMemory property [Windows Update Agent], RecommendedMemory property [Windows Update Agent],IUpdate interface, get_RecommendedMemory, wua.iupdate_recommendedmemory, wuapi/IUpdate::RecommendedMemory, wuapi/IUpdate::get_RecommendedMemory
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
 - IUpdate::get_RecommendedMemory
 - wuapi/IUpdate::get_RecommendedMemory
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
 - IUpdate.RecommendedMemory
 - IUpdate.get_RecommendedMemory
---

# IUpdate::get_RecommendedMemory


## -description

Gets the recommended physical memory size that should be available in your  computer before you install the update. The physical memory size is specified in megabytes (MB).

This property is read-only.

## -parameters

## -remarks

The following properties of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface return 0 (zero) when the information is not available:

<ul>
<li>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed">RecommendedCpuSpeed</a>
</li>
<li>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace">RecommendedHardDiskSpace</a>
</li>
<li><b>RecommendedMemory</b></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>