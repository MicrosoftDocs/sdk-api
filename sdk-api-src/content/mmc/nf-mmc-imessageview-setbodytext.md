---
UID: NF:mmc.IMessageView.SetBodyText
title: IMessageView::SetBodyText (mmc.h)
description: The IMessageView::SetBodyText method enables a snap-in to set the body text for the result pane message displayed using the MMC message OCX control.
helpviewer_keywords: ["IMessageView interface [MMC]","SetBodyText method","IMessageView.SetBodyText","IMessageView::SetBodyText","SetBodyText","SetBodyText method [MMC]","SetBodyText method [MMC]","IMessageView interface","_slate_imessageview_setbodytext","mmc.imessageview_setbodytext","mmc/IMessageView::SetBodyText"]
old-location: mmc\imessageview_setbodytext.htm
tech.root: mmc
ms.assetid: 27b3ae83-be3c-4d40-88b8-9253f1c793f6
ms.date: 12/05/2018
ms.keywords: IMessageView interface [MMC],SetBodyText method, IMessageView.SetBodyText, IMessageView::SetBodyText, SetBodyText, SetBodyText method [MMC], SetBodyText method [MMC],IMessageView interface, _slate_imessageview_setbodytext, mmc.imessageview_setbodytext, mmc/IMessageView::SetBodyText
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
 - IMessageView::SetBodyText
 - mmc/IMessageView::SetBodyText
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
 - IMessageView.SetBodyText
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

MMC creates its own copies of the strings passed to it when the snap-in calls the <a href="/windows/desktop/api/mmc/nf-mmc-imessageview-settitletext">IMessageView::SetTitleText</a> and <b>IMessageView::SetBodyText</b> methods. The snap-in can release the resources at any time after calling 
<b>SetTitleText</b> and 
SetBodyText.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-imessageview">IMessageView</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>