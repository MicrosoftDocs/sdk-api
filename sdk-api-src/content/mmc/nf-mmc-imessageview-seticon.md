---
UID: NF:mmc.IMessageView.SetIcon
title: IMessageView::SetIcon (mmc.h)
description: The IMessageView::SetIcon method enables a snap-in to set the icon for the result pane message displayed using the MMC message OCX control.
helpviewer_keywords: ["IMessageView interface [MMC]","SetIcon method","IMessageView.SetIcon","IMessageView::SetIcon","SetIcon","SetIcon method [MMC]","SetIcon method [MMC]","IMessageView interface","_slate_imessageview_seticon","mmc.imessageview_seticon","mmc/IMessageView::SetIcon"]
old-location: mmc\imessageview_seticon.htm
tech.root: mmc
ms.assetid: 61389d5b-cf0a-465e-9b3b-1bcdef4f92b1
ms.date: 12/05/2018
ms.keywords: IMessageView interface [MMC],SetIcon method, IMessageView.SetIcon, IMessageView::SetIcon, SetIcon, SetIcon method [MMC], SetIcon method [MMC],IMessageView interface, _slate_imessageview_seticon, mmc.imessageview_seticon, mmc/IMessageView::SetIcon
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
 - IMessageView::SetIcon
 - mmc/IMessageView::SetIcon
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
 - IMessageView.SetIcon
---

# IMessageView::SetIcon


## -description

The <b>IMessageView::SetIcon</b> method enables a snap-in to set the icon for the result pane message displayed using the MMC message OCX control.

## -parameters

### -param id [in]

A value that specifies the type of icon for the result pane message. The value is taken from the 
<a href="/windows/desktop/api/mmc/ne-mmc-iconidentifier">IconIdentifier</a> enumeration.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-imessageview">IMessageView</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>