---
UID: NF:mmc.IHeaderCtrl2.SetChangeTimeOut
title: IHeaderCtrl2::SetChangeTimeOut (mmc.h)
author: windows-sdk-content
description: The IHeaderCtrl2::SetChangeTimeOut sets the time-out interval between the time a change takes place in the filter attributes and the posting of an MMCN_FILTER_CHANGE filter change notification, which is sent to the snap-in's IComponent::Notify method.
old-location: mmc\iheaderctrl2_setchangetimeout.htm
tech.root: mmc
ms.assetid: 26a6a9bc-6556-4576-a810-d7c07c07cfd1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl2 interface [MMC],SetChangeTimeOut method, IHeaderCtrl2.SetChangeTimeOut, IHeaderCtrl2::SetChangeTimeOut, SetChangeTimeOut, SetChangeTimeOut method [MMC], SetChangeTimeOut method [MMC],IHeaderCtrl2 interface, _slate_iheaderctrl2_setchangetimeout, mmc.iheaderctrl2_setchangetimeout, mmc/IHeaderCtrl2::SetChangeTimeOut
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IHeaderCtrl2.SetChangeTimeOut
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHeaderCtrl2::SetChangeTimeOut


## -description


The <b>IHeaderCtrl2::SetChangeTimeOut</b> sets the time-out interval between the time a change takes place in the filter attributes and the posting of an 
<a href="https://msdn.microsoft.com/b779f04c-1129-4e05-83c5-fd15ff72f1c2">MMCN_FILTER_CHANGE</a> filter change notification, which is sent to the snap-in's 
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> method.


## -parameters




### -param uTimeout [in]

Filter change interval in milliseconds. The default is an implementation detail of the header control, and as a result MMC does not know about it.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/fecf38be-6f45-45ea-a689-ff37b2b92922">IHeaderCtrl2</a>



<a href="https://msdn.microsoft.com/b779f04c-1129-4e05-83c5-fd15ff72f1c2">MMCN_FILTER_CHANGE</a>
 

 

