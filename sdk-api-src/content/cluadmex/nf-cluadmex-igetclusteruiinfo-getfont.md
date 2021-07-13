---
UID: NF:cluadmex.IGetClusterUIInfo.GetFont
title: IGetClusterUIInfo::GetFont (cluadmex.h)
description: Returns a handle to the font to be displayed on property and wizard pages.
helpviewer_keywords: ["GetFont","GetFont method [Failover Cluster]","GetFont method [Failover Cluster]","IGetClusterUIInfo interface","IGetClusterUIInfo interface [Failover Cluster]","GetFont method","IGetClusterUIInfo.GetFont","IGetClusterUIInfo::GetFont","_wolf_igetclusteruiinfo_getfont","cluadmex/IGetClusterUIInfo::GetFont","mscs.igetclusteruiinfo_getfont"]
old-location: mscs\igetclusteruiinfo_getfont.htm
tech.root: MsCS
ms.assetid: 87dc900d-eee3-4e48-8294-a1d5c3a95179
ms.date: 12/05/2018
ms.keywords: GetFont, GetFont method [Failover Cluster], GetFont method [Failover Cluster],IGetClusterUIInfo interface, IGetClusterUIInfo interface [Failover Cluster],GetFont method, IGetClusterUIInfo.GetFont, IGetClusterUIInfo::GetFont, _wolf_igetclusteruiinfo_getfont, cluadmex/IGetClusterUIInfo::GetFont, mscs.igetclusteruiinfo_getfont
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
 - IGetClusterUIInfo::GetFont
 - cluadmex/IGetClusterUIInfo::GetFont
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
 - IGetClusterUIInfo.GetFont
---

# IGetClusterUIInfo::GetFont


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to the font to be displayed on property and wizard pages.



## -returns

If <b>GetFont</b> is successful, it returns a 
       font handle.

## -remarks

The <b>GetFont</b> method returns the font handle 
     as <b>NULL</b>. 
     <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extensions should not 
     use this return value in their user interface displays.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusteruiinfo">IGetClusterUIInfo</a>
