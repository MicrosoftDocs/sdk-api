---
UID: NF:mmc.IMessageView.SetTitleText
title: IMessageView::SetTitleText
author: windows-sdk-content
description: The IMessageView::SetTitleText method enables a snap-in to set the title text for the result pane message displayed using the MMC message OCX control.
old-location: mmc\imessageview_settitletext.htm
tech.root: mmc
ms.assetid: e041cf74-9fdd-489c-a251-e5b3e55e1bc5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IMessageView interface [MMC],SetTitleText method, IMessageView.SetTitleText, IMessageView::SetTitleText, SetTitleText, SetTitleText method [MMC], SetTitleText method [MMC],IMessageView interface, _slate_imessageview_settitletext, mmc.imessageview_settitletext, mmc/IMessageView::SetTitleText
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMessageView.SetTitleText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmc.h
: 
- IMessageView.SetTitleText
: 
---

# IMessageView::SetTitleText


## -description


The <b>IMessageView::SetTitleText</b> method enables a snap-in to set the title text for the result pane message displayed using the MMC message OCX control.


## -parameters




### -param pszTitleText [in]

A pointer to a null-terminated string that contains the title text for the result pane message.


## -returns



This method can return one of these values.




## -remarks



MMC creates its own copies of the strings passed to it when the snap-in calls the IMessageView::SetTitleText and IMessageView::SetBodyText methods. The snap-in can release the resources at any time after calling 
<b>SetTitleText</b> and 
<b>SetBodyText</b>.




## -see-also




<a href="https://msdn.microsoft.com/e1ea6bb2-f35e-4379-b4e4-70d4e5d77b93">IMessageView</a>



<a href="https://msdn.microsoft.com/bc6db308-d8dd-4868-803d-45c64b951192">Using the MMC Message OCX Control</a>
 

 

