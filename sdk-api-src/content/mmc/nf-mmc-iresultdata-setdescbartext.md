---
UID: NF:mmc.IResultData.SetDescBarText
title: IResultData::SetDescBarText (mmc.h)
description: Sets the description bar text for the result view pane.
helpviewer_keywords: ["IResultData interface [MMC]","SetDescBarText method","IResultData.SetDescBarText","IResultData2 interface [MMC]","SetDescBarText method","IResultData2::SetDescBarText","IResultData::SetDescBarText","SetDescBarText","SetDescBarText method [MMC]","SetDescBarText method [MMC]","IResultData interface","SetDescBarText method [MMC]","IResultData2 interface","_slate_iresultdata_setdescbartext","mmc.iresultdata_setdescbartext","mmc/IResultData2::SetDescBarText","mmc/IResultData::SetDescBarText"]
old-location: mmc\iresultdata_setdescbartext.htm
tech.root: mmc
ms.assetid: e5bde009-9f05-4ecb-9fbc-3ab211baa184
ms.date: 12/05/2018
ms.keywords: IResultData interface [MMC],SetDescBarText method, IResultData.SetDescBarText, IResultData2 interface [MMC],SetDescBarText method, IResultData2::SetDescBarText, IResultData::SetDescBarText, SetDescBarText, SetDescBarText method [MMC], SetDescBarText method [MMC],IResultData interface, SetDescBarText method [MMC],IResultData2 interface, _slate_iresultdata_setdescbartext, mmc.iresultdata_setdescbartext, mmc/IResultData2::SetDescBarText, mmc/IResultData::SetDescBarText
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
 - IResultData::SetDescBarText
 - mmc/IResultData::SetDescBarText
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
 - IResultData.SetDescBarText
 - IResultData2.SetDescBarText
---

# IResultData::SetDescBarText


## -description

The <b>IResultData::SetDescBarText</b> method sets the description bar text for the result view pane.

## -parameters

### -param DescText [in]

A pointer to a null-terminated string that contains text to be displayed in the description bar.

## -returns

This method can return one of these values.

## -remarks

This method provides the same functionality for both result view panes and virtual lists.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>