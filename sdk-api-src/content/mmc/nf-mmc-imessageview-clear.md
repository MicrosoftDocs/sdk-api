---
UID: NF:mmc.IMessageView.Clear
title: IMessageView::Clear
author: windows-sdk-content
description: The IMessageView::Clear method enables a snap-in to clear the title, text, and icon of the result pane message displayed using the MMC message OCX control.
old-location: mmc\imessageview_clear.htm
tech.root: MMC
ms.assetid: 495b92bf-1629-49f5-917c-290151c9176e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Clear, Clear method [MMC], Clear method [MMC],IMessageView interface, IMessageView interface [MMC],Clear method, IMessageView.Clear, IMessageView::Clear, _slate_imessageview_clear, mmc.imessageview_clear, mmc/IMessageView::Clear
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
 - IMessageView.Clear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMessageView::Clear


## -description


The <b>IMessageView::Clear</b> method enables a snap-in to clear the title, text, and icon of the result pane message displayed using the MMC message OCX control.


## -parameters






## -returns



This method can return one of these values.




## -remarks



The 
Clear method provides a way to reset the content of the message, but the snap-in is not required to call this method to release resources. MMC creates its own copies of the strings passed to it when the snap-in calls the <a href="https://msdn.microsoft.com/e041cf74-9fdd-489c-a251-e5b3e55e1bc5">IMessageView::SetTitleText</a> and <a href="https://msdn.microsoft.com/27b3ae83-be3c-4d40-88b8-9253f1c793f6">IMessageView::SetBodyText</a> methods. The snap-in can release the resources after calling 
SetTitleText and 
SetBodyText.




## -see-also




<a href="https://msdn.microsoft.com/e1ea6bb2-f35e-4379-b4e4-70d4e5d77b93">IMessageView</a>



<a href="https://msdn.microsoft.com/bc6db308-d8dd-4868-803d-45c64b951192">Using the MMC Message OCX Control</a>
 

 

