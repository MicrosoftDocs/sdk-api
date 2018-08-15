---
UID: NF:effects.IWMPEffects.DisplayPropertyPage
title: IWMPEffects::DisplayPropertyPage
author: windows-sdk-content
description: The DisplayPropertyPage method displays the property page of a visualization, if it exists.
old-location: wmp\iwmpeffects_displaypropertypage.htm
old-project: WMP
ms.assetid: dadde782-577d-4dcb-b8ae-2f6ddca77a40
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DisplayPropertyPage, DisplayPropertyPage method [Windows Media Player], DisplayPropertyPage method [Windows Media Player],IWMPEffects interface, EffectsDisplayPropertyPage, IWMPEffects interface [Windows Media Player],DisplayPropertyPage method, IWMPEffects.DisplayPropertyPage, IWMPEffects::DisplayPropertyPage, effects/IWMPEffects::DisplayPropertyPage, wmp.iwmpeffects_displaypropertypage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: effects.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
req.target-min-winversvr: 
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects.DisplayPropertyPage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IWMPEffects::DisplayPropertyPage


## -description



The <b>DisplayPropertyPage</b> method displays the property page of a visualization, if it exists.




## -parameters




### -param hwndOwner [in]

Handle to the dialog that will be displayed.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Implement this method if you want to display a property page to the user to adjust any values of the visualization.




## -see-also




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>
 

 

