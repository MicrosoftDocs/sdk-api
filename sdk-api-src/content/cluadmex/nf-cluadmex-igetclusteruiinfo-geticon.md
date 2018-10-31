---
UID: NF:cluadmex.IGetClusterUIInfo.GetIcon
title: IGetClusterUIInfo::GetIcon
author: windows-sdk-content
description: Returns a handle to the icon to use in the upper-left corner of property and wizard pages.
old-location: mscs\igetclusteruiinfo_geticon.htm
tech.root: mscs
ms.assetid: b4572178-6225-4a22-8b45-7e8abbaa9759
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetIcon, GetIcon method [Failover Cluster], GetIcon method [Failover Cluster],IGetClusterUIInfo interface, IGetClusterUIInfo interface [Failover Cluster],GetIcon method, IGetClusterUIInfo.GetIcon, IGetClusterUIInfo::GetIcon, _wolf_igetclusteruiinfo_geticon, cluadmex/IGetClusterUIInfo::GetIcon, mscs.igetclusteruiinfo_geticon
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
 - IGetClusterUIInfo.GetIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterUIInfo::GetIcon


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to the icon to use in the upper-left corner of property and wizard pages.


## -parameters






## -returns



<b>GetIcon</b> always returns a handle to an 
       icon.




## -remarks



With the <b>GetIcon</b> method, each property page 
     or wizard page should have an icon control positioned at (8,7) with a size of (18,20).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370234(v=VS.85).aspx">IGetClusterUIInfo</a>
 

 

