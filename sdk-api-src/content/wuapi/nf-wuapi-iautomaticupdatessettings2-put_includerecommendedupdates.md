---
UID: NF:wuapi.IAutomaticUpdatesSettings2.put_IncludeRecommendedUpdates
title: IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates
author: windows-sdk-content
description: Gets and sets a Boolean value that indicates whether to include optional or recommended updates when a search for updates and installation of updates is performed.
old-location: wua\iautomaticupdatessettings2_includerecommendedupdates.htm
old-project: Wua_Sdk
ms.assetid: 502b0490-8834-496a-8691-d9325ad86799
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IAutomaticUpdatesSettings2 interface [Windows Update Agent],IncludeRecommendedUpdates property, IAutomaticUpdatesSettings2.IncludeRecommendedUpdates, IAutomaticUpdatesSettings2.put_IncludeRecommendedUpdates, IAutomaticUpdatesSettings2::IncludeRecommendedUpdates, IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates, IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates, IncludeRecommendedUpdates property [Windows Update Agent], IncludeRecommendedUpdates property [Windows Update Agent],IAutomaticUpdatesSettings2 interface, put_IncludeRecommendedUpdates, wua.iautomaticupdatessettings2_includerecommendedupdates, wuapi/IAutomaticUpdatesSettings2::IncludeRecommendedUpdates, wuapi/IAutomaticUpdatesSettings2::get_IncludeRecommendedUpdates, wuapi/IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesSettings2.IncludeRecommendedUpdates
 - IAutomaticUpdatesSettings2.get_IncludeRecommendedUpdates
 - IAutomaticUpdatesSettings2.put_IncludeRecommendedUpdates
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAutomaticUpdatesSettings2::put_IncludeRecommendedUpdates


## -description


<p class="CCE_Message">[<b>Set</b> is no longer supported. Also, starting with 
    Windows 10 calls to <b>Get</b> always return <b>VARIANT_TRUE</b> (include recommended updates). ]


Gets and sets a Boolean value that indicates whether to include optional or recommended updates when a  search for updates and installation of updates is performed.



This property is read/write.


## -parameters


## -remarks



Only administrators can set this property.

The caller can modify the settings in  the <a href="https://msdn.microsoft.com/5ad1a3ee-3293-4825-a85e-ca1e3a38e775">IAutomaticUpdatesSettings2</a> interface only if the <a href="https://msdn.microsoft.com/e7a066b9-9581-4573-82e2-a6f2ca7440ac">ReadOnly</a> property is <b>VARIANT_TRUE</b>.
The <b>ReadOnly</b> property may change after the <a href="https://msdn.microsoft.com/308426d9-d524-406a-931c-1fdb854aa4fb">Refresh</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/5ad1a3ee-3293-4825-a85e-ca1e3a38e775">IAutomaticUpdatesSettings2</a>
 

 

