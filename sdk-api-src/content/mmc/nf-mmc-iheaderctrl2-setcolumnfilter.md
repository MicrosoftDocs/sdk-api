---
UID: NF:mmc.IHeaderCtrl2.SetColumnFilter
title: IHeaderCtrl2::SetColumnFilter (mmc.h)
description: The IHeaderCtrl2::SetColumnFilter sets the filter value and its maximum character length for a specified column in a filtered list.
old-location: mmc\iheaderctrl2_setcolumnfilter.htm
tech.root: mmc
ms.assetid: df1257ee-66c4-4b63-a9c5-1bd0b94b4a85
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl2 interface [MMC],SetColumnFilter method, IHeaderCtrl2.SetColumnFilter, IHeaderCtrl2::SetColumnFilter, SetColumnFilter, SetColumnFilter method [MMC], SetColumnFilter method [MMC],IHeaderCtrl2 interface, _slate_iheaderctrl2_setcolumnfilter, mmc.iheaderctrl2_setcolumnfilter, mmc/IHeaderCtrl2::SetColumnFilter
f1_keywords:
- mmc/IHeaderCtrl2.SetColumnFilter
dev_langs:
- c++
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
- IHeaderCtrl2.SetColumnFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHeaderCtrl2::SetColumnFilter


## -description


The <b>IHeaderCtrl2::SetColumnFilter</b> sets the filter value and its maximum character length for a specified column in a filtered list.


## -parameters




### -param nColumn [in]

A zero-based index that identifies the column for which the filter value and its maximum character length are to be set.


### -param dwType [in]

Filter type to apply to the specified column, taken from the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ne-mmc-mmc_filter_type">MMC_FILTER_TYPE</a> enumeration.


### -param pFilterData [in]

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-mmc_filterdata">MMC_FILTERDATA</a> structure that holds the actual filter data.


## -returns



This method can return one of these values.




## -remarks



For both setting and reading filter values, the snap-in owns the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-mmc_filterdata">MMC_FILTERDATA</a> structure and any text buffer.

If the snap-in does not explicitly set the filter data for a column in a filtered list by calling <b>IHeaderCtrl2::SetColumnFilter</b>, the filter type defaults to MMC_STRING_FILTER with no default value for the filter (MMC_FILTER_NOVALUE). The default length of the filter is not documented by the Win32 header control, but it is of sufficient length for most likely user inputs. If the snap-in requires a specific length, it should call <b>IHeaderCtrl2::SetColumnFilter</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iheaderctrl2">IHeaderCtrl2</a>
 

 

