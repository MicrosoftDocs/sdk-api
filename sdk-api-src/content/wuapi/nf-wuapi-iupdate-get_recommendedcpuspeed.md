---
UID: NF:wuapi.IUpdate.get_RecommendedCpuSpeed
title: IUpdate::get_RecommendedCpuSpeed (wuapi.h)
description: Gets the recommended CPU speed used to install the update, in megahertz (MHz).
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","RecommendedCPUSpeed property","IUpdate.RecommendedCPUSpeed","IUpdate.get_RecommendedCpuSpeed","IUpdate::RecommendedCPUSpeed","IUpdate::get_RecommendedCPUSpeed","IUpdate::get_RecommendedCpuSpeed","RecommendedCPUSpeed property [Windows Update Agent]","RecommendedCPUSpeed property [Windows Update Agent]","IUpdate interface","get_RecommendedCpuSpeed","wua.iupdate_recommendedcpuspeed","wuapi/IUpdate::RecommendedCPUSpeed","wuapi/IUpdate::get_RecommendedCPUSpeed"]
old-location: wua\iupdate_recommendedcpuspeed.htm
tech.root: wua
ms.assetid: 21003be2-c14e-48d4-a51f-ed75b1b47284
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],RecommendedCPUSpeed property, IUpdate.RecommendedCPUSpeed, IUpdate.get_RecommendedCpuSpeed, IUpdate::RecommendedCPUSpeed, IUpdate::get_RecommendedCPUSpeed, IUpdate::get_RecommendedCpuSpeed, RecommendedCPUSpeed property [Windows Update Agent], RecommendedCPUSpeed property [Windows Update Agent],IUpdate interface, get_RecommendedCpuSpeed, wua.iupdate_recommendedcpuspeed, wuapi/IUpdate::RecommendedCPUSpeed, wuapi/IUpdate::get_RecommendedCPUSpeed
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
 - IUpdate::get_RecommendedCpuSpeed
 - wuapi/IUpdate::get_RecommendedCpuSpeed
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
 - IUpdate.RecommendedCPUSpeed
 - IUpdate.get_RecommendedCPUSpeed
---

# IUpdate::get_RecommendedCpuSpeed


## -description

Gets the recommended CPU speed used to install the update, in megahertz (MHz).

This property is read-only.

## -parameters

## -remarks

The following properties of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface return 0 (zero) when the information is not available:

<ul>
<li><b>RecommendedCpuSpeed</b></li>
<li>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace">RecommendedHardDiskSpace</a>
</li>
<li>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedmemory">RecommendedMemory</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>