---
UID: NF:wmp.IWMPEvents.CurrentItemChange
title: IWMPEvents::CurrentItemChange
author: windows-sdk-content
description: The CurrentItemChange event occurs when the user or the IWMPControls::put_CurrentItem method changes the current item value.
old-location: wmp\iwmpevents_iwmpevents__currentitemchange.htm
old-project: WMP
ms.assetid: 3669fe6e-233e-4214-9f84-763a06835f48
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CurrentItemChange, CurrentItemChange method [Windows Media Player], CurrentItemChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CurrentItemChange method, IWMPEvents.CurrentItemChange, IWMPEvents::CurrentItemChange, IWMPEventsCurrentItemChange, wmp.iwmpevents_iwmpevents__currentitemchange, wmp/IWMPEvents::CurrentItemChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.CurrentItemChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::CurrentItemChange


## -description



The <b>CurrentItemChange</b> event occurs when the user or the <b>IWMPControls::put_CurrentItem</b> method changes the current item value.




## -parameters




### -param pdispMedia [in]

Pointer to an <b>IDispatch</b> interface that identifies the new current item.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/190cec53-5cd9-4bd0-b8d9-23c5389fe231">IWMPControls::put_currentItem</a>



<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

