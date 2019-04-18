---
UID: NF:mmc.IControlbar.Attach
title: IControlbar::Attach (mmc.h)
author: windows-sdk-content
description: The IControlbar::Attach method allows the snap-in to associate a control with a control bar.
old-location: mmc\icontrolbar_attach.htm
tech.root: mmc
ms.assetid: 60ed8f9a-d5ad-4a68-8019-6887104c9b2a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Attach, Attach method [MMC], Attach method [MMC],IControlbar interface, IControlbar interface [MMC],Attach method, IControlbar.Attach, IControlbar::Attach, _slate_icontrolbar_attach, mmc.icontrolbar_attach, mmc/IControlbar::Attach
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
 - IControlbar.Attach
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IControlbar::Attach


## -description


The <b>IControlbar::Attach</b> method allows the snap-in to associate a control with a control bar.


## -parameters




### -param nType [in]

A value that specifies the type of control to be associated with the control bar, taken from the 
<a href="https://msdn.microsoft.com/f4f64769-a3d0-46eb-8520-a6cb7237d007">MMC_CONTROL_TYPE</a> enumeration.


### -param lpUnknown [in]

A pointer to the IUnknown interface on the control object to be inserted.


## -returns



This method can return one of these values.




## -remarks



Although COMBOBOXBAR appears in Mmc.idl in connection with the nType parameter, it is not implemented.




## -see-also




<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

