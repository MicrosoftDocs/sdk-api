---
UID: NF:cluadmex.IGetClusterUIInfo.GetLocale
title: IGetClusterUIInfo::GetLocale (cluadmex.h)
description: Returns the locale identifier to be used with property and wizard pages.
helpviewer_keywords: ["GetLocale","GetLocale method [Failover Cluster]","GetLocale method [Failover Cluster]","IGetClusterUIInfo interface","IGetClusterUIInfo interface [Failover Cluster]","GetLocale method","IGetClusterUIInfo.GetLocale","IGetClusterUIInfo::GetLocale","_wolf_igetclusteruiinfo_getlocale","cluadmex/IGetClusterUIInfo::GetLocale","mscs.igetclusteruiinfo_getlocale"]
old-location: mscs\igetclusteruiinfo_getlocale.htm
tech.root: MsCS
ms.assetid: 1ab4e6bb-0aba-4115-b068-171aaf0b7cef
ms.date: 12/05/2018
ms.keywords: GetLocale, GetLocale method [Failover Cluster], GetLocale method [Failover Cluster],IGetClusterUIInfo interface, IGetClusterUIInfo interface [Failover Cluster],GetLocale method, IGetClusterUIInfo.GetLocale, IGetClusterUIInfo::GetLocale, _wolf_igetclusteruiinfo_getlocale, cluadmex/IGetClusterUIInfo::GetLocale, mscs.igetclusteruiinfo_getlocale
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
 - IGetClusterUIInfo::GetLocale
 - cluadmex/IGetClusterUIInfo::GetLocale
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
 - IGetClusterUIInfo.GetLocale
---

# IGetClusterUIInfo::GetLocale


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the locale identifier to be used with property and wizard pages.



## -returns

<b>GetLocale</b> always returns the locale 
       identifier for the cluster.

## -remarks

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extensions call the 
     <b>GetLocale</b> method to retrieve the locale 
     identifier that can be used for loading dialog resources. A single Failover Cluster Administrator extension DLL 
     can support multiple languages.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusteruiinfo">IGetClusterUIInfo</a>
