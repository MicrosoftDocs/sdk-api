---
UID: NF:mmc.IMessageView.Clear
title: IMessageView::Clear (mmc.h)
description: The IMessageView::Clear method enables a snap-in to clear the title, text, and icon of the result pane message displayed using the MMC message OCX control.
helpviewer_keywords: ["Clear","Clear method [MMC]","Clear method [MMC]","IMessageView interface","IMessageView interface [MMC]","Clear method","IMessageView.Clear","IMessageView::Clear","_slate_imessageview_clear","mmc.imessageview_clear","mmc/IMessageView::Clear"]
old-location: mmc\imessageview_clear.htm
tech.root: mmc
ms.assetid: 495b92bf-1629-49f5-917c-290151c9176e
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [MMC], Clear method [MMC],IMessageView interface, IMessageView interface [MMC],Clear method, IMessageView.Clear, IMessageView::Clear, _slate_imessageview_clear, mmc.imessageview_clear, mmc/IMessageView::Clear
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMessageView::Clear
 - mmc/IMessageView::Clear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IMessageView.Clear
---

# IMessageView::Clear


## -description

The <b>IMessageView::Clear</b> method enables a snap-in to clear the title, text, and icon of the result pane message displayed using the MMC message OCX control.



## -returns

This method can return one of these values.

## -remarks

The 
Clear method provides a way to reset the content of the message, but the snap-in is not required to call this method to release resources. MMC creates its own copies of the strings passed to it when the snap-in calls the <a href="/windows/desktop/api/mmc/nf-mmc-imessageview-settitletext">IMessageView::SetTitleText</a> and <a href="/windows/desktop/api/mmc/nf-mmc-imessageview-setbodytext">IMessageView::SetBodyText</a> methods. The snap-in can release the resources after calling 
SetTitleText and 
SetBodyText.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-imessageview">IMessageView</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>
