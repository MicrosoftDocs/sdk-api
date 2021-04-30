---
UID: NF:mmc.IHeaderCtrl2.GetColumnFilter
title: IHeaderCtrl2::GetColumnFilter (mmc.h)
description: The IHeaderCtrl2::GetColumnFilter method retrieves the filter value set on the specified column.
helpviewer_keywords: ["GetColumnFilter","GetColumnFilter method [MMC]","GetColumnFilter method [MMC]","IHeaderCtrl2 interface","IHeaderCtrl2 interface [MMC]","GetColumnFilter method","IHeaderCtrl2.GetColumnFilter","IHeaderCtrl2::GetColumnFilter","_slate_iheaderctrl2_getcolumnfilter","mmc.iheaderctrl2_getcolumnfilter","mmc/IHeaderCtrl2::GetColumnFilter"]
old-location: mmc\iheaderctrl2_getcolumnfilter.htm
tech.root: mmc
ms.assetid: 2daf15ac-4de2-422d-9ac0-b592090468ed
ms.date: 12/05/2018
ms.keywords: GetColumnFilter, GetColumnFilter method [MMC], GetColumnFilter method [MMC],IHeaderCtrl2 interface, IHeaderCtrl2 interface [MMC],GetColumnFilter method, IHeaderCtrl2.GetColumnFilter, IHeaderCtrl2::GetColumnFilter, _slate_iheaderctrl2_getcolumnfilter, mmc.iheaderctrl2_getcolumnfilter, mmc/IHeaderCtrl2::GetColumnFilter
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
 - IHeaderCtrl2::GetColumnFilter
 - mmc/IHeaderCtrl2::GetColumnFilter
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
 - IHeaderCtrl2.GetColumnFilter
---

# IHeaderCtrl2::GetColumnFilter


## -description

The <b>IHeaderCtrl2::GetColumnFilter</b> method retrieves the filter value set on the specified column.

## -parameters

### -param nColumn [in]

A zero-based index that identifies the column for which the filter value and its maximum character length are to be retrieved.

### -param pdwType [in, out]

A pointer to a variable of type <b>DWORD</b> that can take one of the possible filter values specified in the 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_filter_type">MMC_FILTER_TYPE</a> enumeration. The filter type for the specified column is placed in the address pointed to by <i>pdwType</i>.

### -param pFilterData [in, out]

A pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_filterdata">MMC_FILTERDATA</a> structure that holds the actual filter data.

## -returns

This method can return one of these values.

## -remarks

For both setting and reading filter values, the snap-in owns the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_filterdata">MMC_FILTERDATA</a> structure and any text buffer.

When reading a filter value, if the filter type specified by the snap-in does not match the current type, the <b>IHeaderCtrl2::GetColumnFilter</b> method will return <b>E_FAIL</b>. On receiving an <b>E_FAIL</b>, the values returned by the method are undefined.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iheaderctrl2">IHeaderCtrl2</a>