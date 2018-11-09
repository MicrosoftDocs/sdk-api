---
UID: NF:cluadmex.IGetClusterUIInfo.GetLocale
title: IGetClusterUIInfo::GetLocale
author: windows-sdk-content
description: Returns the locale identifier to be used with property and wizard pages.
old-location: mscs\igetclusteruiinfo_getlocale.htm
tech.root: mscs
ms.assetid: 1ab4e6bb-0aba-4115-b068-171aaf0b7cef
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: GetLocale, GetLocale method [Failover Cluster], GetLocale method [Failover Cluster],IGetClusterUIInfo interface, IGetClusterUIInfo interface [Failover Cluster],GetLocale method, IGetClusterUIInfo.GetLocale, IGetClusterUIInfo::GetLocale, _wolf_igetclusteruiinfo_getlocale, cluadmex/IGetClusterUIInfo::GetLocale, mscs.igetclusteruiinfo_getlocale
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterUIInfo.GetLocale
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterUIInfo::GetLocale


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the locale identifier to be used with property and wizard pages.


## -parameters






## -returns



<b>GetLocale</b> always returns the locale 
       identifier for the cluster.




## -remarks




<a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extensions call the 
     <b>GetLocale</b> method to retrieve the locale 
     identifier that can be used for loading dialog resources. A single Failover Cluster Administrator extension DLL 
     can support multiple languages.




## -see-also




<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>
 

 

