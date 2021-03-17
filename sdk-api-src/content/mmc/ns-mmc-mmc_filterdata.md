---
UID: NS:mmc._MMC_FILTERDATA
title: MMC_FILTERDATA (mmc.h)
description: The MMC_FILTERDATA structure is introduced in MMC 1.2.
helpviewer_keywords: ["MMC_FILTERDATA","MMC_FILTERDATA structure [MMC]","_slate_mmc_filterdata","mmc.mmc_filterdata","mmc/MMC_FILTERDATA"]
old-location: mmc\mmc_filterdata.htm
tech.root: mmc
ms.assetid: 312d27b8-cfca-48fd-8d39-b0f504421d2d
ms.date: 12/05/2018
ms.keywords: MMC_FILTERDATA, MMC_FILTERDATA structure [MMC], _slate_mmc_filterdata, mmc.mmc_filterdata, mmc/MMC_FILTERDATA
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
req.typenames: MMC_FILTERDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_FILTERDATA
 - mmc/_MMC_FILTERDATA
 - MMC_FILTERDATA
 - mmc/MMC_FILTERDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_FILTERDATA
---

# MMC_FILTERDATA structure


## -description

The 
MMC_FILTERDATA structure is introduced in MMC 1.2.

The 
MMC_FILTERDATA structure is used by the 
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-getcolumnfilter">IHeaderCtrl2::GetColumnFilter</a> and 
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-setcolumnfilter">IHeaderCtrl2::SetColumnFilter</a> methods to retrieve and set the filter value of a column in a filtered list view.

## -struct-fields

### -field pszText

When a snap-in sets a text filter value, pszText points to the filter string to set and cchTextMax sets the maximum length of the filter string that the user can type into the filter field. When a snap-in reads a text filter value, pszText points to a buffer to receive the text and cchTextMax gives the length of the buffer.

### -field cchTextMax

For more information, see the description for pszText.

### -field lValue

When a snap-in sets a numeric filter value, lValue contains the filter value. The filter field converts the value to a string and places it in the filter control. When a snap-in reads a numeric filter value, the current filter value is converted to binary and returned in lValue.

## -remarks

A numeric filter value can be used when the column it is filtering has only numeric values rather than arbitrary text strings. The advantage of using a numeric filter is that the filter handles the conversion between the binary and text when setting and reading the filter value. Also the filter control only allows a user to type numeric characters into a numeric filter.

When handling a text filter, lValue is ignored. Similarly, when handling a numeric filter, pszText and cchTextMax are ignored.

For both setting and reading filter values, the snap-in owns the 
MMC_FILTERDATA structure and any text buffer.