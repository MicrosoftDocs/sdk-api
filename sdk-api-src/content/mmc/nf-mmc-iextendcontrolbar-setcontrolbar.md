---
UID: NF:mmc.IExtendControlbar.SetControlbar
title: IExtendControlbar::SetControlbar
author: windows-sdk-content
description: The IExtendControlbar::SetControlbar method attaches or detaches a control bar.
old-location: mmc\iextendcontrolbar_setcontrolbar.htm
old-project: mmc
ms.assetid: 5088eff2-b7a0-4c16-a33c-3a82bc2e72af
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IExtendControlbar interface [MMC],SetControlbar method, IExtendControlbar.SetControlbar, IExtendControlbar::SetControlbar, SetControlbar, SetControlbar method [MMC], SetControlbar method [MMC],IExtendControlbar interface, _slate_iextendcontrolbar_setcontrolbar, mmc.iextendcontrolbar_setcontrolbar, mmc/IExtendControlbar::SetControlbar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
 - Mmc.h
api_name:
 - IExtendControlbar.SetControlbar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IExtendControlbar::SetControlbar


## -description


The <b>IExtendControlbar::SetControlbar</b> method attaches or detaches a control bar.


## -parameters




### -param pControlbar [in]

A pointer to an 
<a href="https://msdn.microsoft.com/8ba12331-34e8-46ff-ab66-a6ada3d731f6">IControlbar</a> interface on the control bar object to be set. A non-<b>NULL</b> value attaches a control bar; a <b>NULL</b> value detaches a control bar.


## -returns



This method can return one of these values.




## -remarks



As items are selected and deselected, snap-ins are activated and deactivated. When a snap-in is activated, the console calls 
SetControlbar with a non-<b>NULL</b> pControlbar value. The snap-in should call AddRef on this IControlBar. The snap-in should also use this opportunity to attach controls. Similarly, when the snap-in is deactivated, the console calls 
SetControlbar with a <b>NULL</b> pControlbar. The snap-in should then detach its controls and call Release on the saved IControlBar.




## -see-also




<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

