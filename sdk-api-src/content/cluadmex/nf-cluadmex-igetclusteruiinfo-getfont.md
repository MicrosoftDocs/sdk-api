---
UID: NF:cluadmex.IGetClusterUIInfo.GetFont
title: IGetClusterUIInfo::GetFont
author: windows-sdk-content
description: Returns a handle to the font to be displayed on property and wizard pages.
old-location: mscs\igetclusteruiinfo_getfont.htm
old-project: mscs
ms.assetid: 87dc900d-eee3-4e48-8294-a1d5c3a95179
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFont, GetFont method [Failover Cluster], GetFont method [Failover Cluster],IGetClusterUIInfo interface, IGetClusterUIInfo interface [Failover Cluster],GetFont method, IGetClusterUIInfo.GetFont, IGetClusterUIInfo::GetFont, _wolf_igetclusteruiinfo_getfont, cluadmex/IGetClusterUIInfo::GetFont, mscs.igetclusteruiinfo_getfont
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterUIInfo.GetFont
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterUIInfo::GetFont


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to the font to be displayed on property and wizard pages.


## -parameters






## -returns



If <b>GetFont</b> is successful, it returns a 
       font handle.




## -remarks



The <b>GetFont</b> method returns the font handle 
     as <b>NULL</b>. 
     <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extensions should not 
     use this return value in their user interface displays.




## -see-also




<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>
 

 

