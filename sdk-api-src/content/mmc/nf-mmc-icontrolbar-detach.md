---
UID: NF:mmc.IControlbar.Detach
title: IControlbar::Detach
author: windows-sdk-content
description: The IControlbar::Detach method breaks the association between a control and the control bar. This command removes or detaches the control from the control bar on which it is displayed.
old-location: mmc\icontrolbar_detach.htm
old-project: mmc
ms.assetid: a40fc3a4-40ff-4752-abd9-e4dd906bc27f
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: Detach, Detach method [MMC], Detach method [MMC],IControlbar interface, IControlbar interface [MMC],Detach method, IControlbar.Detach, IControlbar::Detach, _slate_icontrolbar_detach, mmc.icontrolbar_detach, mmc/IControlbar::Detach
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IControlbar.Detach
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IControlbar::Detach


## -description


The <b>IControlbar::Detach</b> method breaks the association between a control and the control bar. This command removes or detaches the control from the control bar on which it is displayed.


## -parameters




### -param lpUnknown [in]

A pointer to the 
<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface on the control object that represents the control removed.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

