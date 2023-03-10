---
UID: NN:mmc.IResultDataCompare
title: IResultDataCompare (mmc.h)
description: Allows primary snap-ins to compare result items that are displayed in a sorted order in the result pane.
helpviewer_keywords: ["IResultDataCompare","IResultDataCompare interface [MMC]","IResultDataCompare interface [MMC]","described","_slate_iresultdatacompare","mmc.iresultdatacompare","mmc/IResultDataCompare"]
old-location: mmc\iresultdatacompare.htm
tech.root: mmc
ms.assetid: 7a68713c-2de5-4944-a617-0b2d46c23eea
ms.date: 12/05/2018
ms.keywords: IResultDataCompare, IResultDataCompare interface [MMC], IResultDataCompare interface [MMC],described, _slate_iresultdatacompare, mmc.iresultdatacompare, mmc/IResultDataCompare
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResultDataCompare
 - mmc/IResultDataCompare
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultDataCompare
---

# IResultDataCompare interface


## -description

The 
<b>IResultDataCompare</b> interface allows primary snap-ins to compare result items that are displayed in a sorted order in the result pane. MMC uses a primary snap-in's implementation of this interface for all results items. Scope items from either the primary snap-in or any extensions are left unsorted at the top of the list.

The 
<b>IResultDataCompare</b> interface differs from the 
<a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompareex">IResultDataCompareEx</a> interface. 
<b>IResultDataCompareEx</b> allows primary snap-ins to compare both scope and result items.

## -inheritance

The <b>IResultDataCompare</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultDataCompare</b> also has these types of members:

