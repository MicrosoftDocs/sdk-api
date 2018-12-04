---
UID: NF:mmc.IMessageView.SetBodyText
title: IMessageView::SetBodyText
author: windows-sdk-content
description: The IMessageView::SetBodyText method enables a snap-in to set the body text for the result pane message displayed using the MMC message OCX control.
old-location: mmc\imessageview_setbodytext.htm
tech.root: mmc
ms.assetid: 27b3ae83-be3c-4d40-88b8-9253f1c793f6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMessageView interface [MMC],SetBodyText method, IMessageView.SetBodyText, IMessageView::SetBodyText, SetBodyText, SetBodyText method [MMC], SetBodyText method [MMC],IMessageView interface, _slate_imessageview_setbodytext, mmc.imessageview_setbodytext, mmc/IMessageView::SetBodyText
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
 - IMessageView.SetBodyText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMessageView::SetBodyText


## -description


The <b>IMessageView::SetBodyText</b> method enables a snap-in to set the body text for the result pane message displayed using the MMC message OCX control.


## -parameters




### -param pszBodyText [in]

A pointer to a null-terminated string that contains the body text for the result pane message.


## -returns



This method can return one of these values.




## -remarks



MMC creates its own copies of the strings passed to it when the snap-in calls the <a href="https://msdn.microsoft.com/e041cf74-9fdd-489c-a251-e5b3e55e1bc5">IMessageView::SetTitleText</a> and <b>IMessageView::SetBodyText</b> methods. The snap-in can release the resources at any time after calling 
<b>SetTitleText</b> and 
SetBodyText.




## -see-also




<a href="https://msdn.microsoft.com/e1ea6bb2-f35e-4379-b4e4-70d4e5d77b93">IMessageView</a>



<a href="https://msdn.microsoft.com/bc6db308-d8dd-4868-803d-45c64b951192">Using the MMC Message OCX Control</a>
 

 

