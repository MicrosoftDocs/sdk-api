---
UID: NF:mmc.IMessageView.SetTitleText
title: IMessageView::SetTitleText (mmc.h)
description: The IMessageView::SetTitleText method enables a snap-in to set the title text for the result pane message displayed using the MMC message OCX control.
helpviewer_keywords: ["IMessageView interface [MMC]","SetTitleText method","IMessageView.SetTitleText","IMessageView::SetTitleText","SetTitleText","SetTitleText method [MMC]","SetTitleText method [MMC]","IMessageView interface","_slate_imessageview_settitletext","mmc.imessageview_settitletext","mmc/IMessageView::SetTitleText"]
old-location: mmc\imessageview_settitletext.htm
tech.root: mmc
ms.assetid: e041cf74-9fdd-489c-a251-e5b3e55e1bc5
ms.date: 12/05/2018
ms.keywords: IMessageView interface [MMC],SetTitleText method, IMessageView.SetTitleText, IMessageView::SetTitleText, SetTitleText, SetTitleText method [MMC], SetTitleText method [MMC],IMessageView interface, _slate_imessageview_settitletext, mmc.imessageview_settitletext, mmc/IMessageView::SetTitleText
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
 - IMessageView::SetTitleText
 - mmc/IMessageView::SetTitleText
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
 - IMessageView.SetTitleText
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

<a href="/windows/desktop/api/mmc/nn-mmc-imessageview">IMessageView</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>