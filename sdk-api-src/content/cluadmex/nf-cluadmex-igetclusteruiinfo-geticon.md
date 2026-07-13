---
UID: NF:cluadmex.IGetClusterUIInfo.GetIcon
title: IGetClusterUIInfo::GetIcon (cluadmex.h)
description: Returns a handle to the icon to use in the upper-left corner of property and wizard pages.
helpviewer_keywords: ["GetIcon","GetIcon method [Failover Cluster]","GetIcon method [Failover Cluster]","IGetClusterUIInfo interface","IGetClusterUIInfo interface [Failover Cluster]","GetIcon method","IGetClusterUIInfo.GetIcon","IGetClusterUIInfo::GetIcon","_wolf_igetclusteruiinfo_geticon","cluadmex/IGetClusterUIInfo::GetIcon","mscs.igetclusteruiinfo_geticon"]
old-location: mscs\igetclusteruiinfo_geticon.htm
tech.root: MsCS
ms.assetid: b4572178-6225-4a22-8b45-7e8abbaa9759
ms.date: 12/05/2018
ms.keywords: GetIcon, GetIcon method [Failover Cluster], GetIcon method [Failover Cluster],IGetClusterUIInfo interface, IGetClusterUIInfo interface [Failover Cluster],GetIcon method, IGetClusterUIInfo.GetIcon, IGetClusterUIInfo::GetIcon, _wolf_igetclusteruiinfo_geticon, cluadmex/IGetClusterUIInfo::GetIcon, mscs.igetclusteruiinfo_geticon
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
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
 - IGetClusterUIInfo::GetIcon
 - cluadmex/IGetClusterUIInfo::GetIcon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterUIInfo.GetIcon
---

# IGetClusterUIInfo::GetIcon


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to the icon to use in the upper-left corner of property and wizard pages.



## -returns

<b>GetIcon</b> always returns a handle to an 
       icon.

## -remarks

With the <b>GetIcon</b> method, each property page 
     or wizard page should have an icon control positioned at (8,7) with a size of (18,20).

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusteruiinfo">IGetClusterUIInfo</a>
