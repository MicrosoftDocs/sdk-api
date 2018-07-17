---
UID: NF:mmc.IHeaderCtrl2.SetColumnFilter
title: IHeaderCtrl2::SetColumnFilter
author: windows-sdk-content
description: The IHeaderCtrl2::SetColumnFilter sets the filter value and its maximum character length for a specified column in a filtered list.
old-location: mmc\iheaderctrl2_setcolumnfilter.htm
old-project: mmc
ms.assetid: df1257ee-66c4-4b63-a9c5-1bd0b94b4a85
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: IHeaderCtrl2 interface [MMC],SetColumnFilter method, IHeaderCtrl2.SetColumnFilter, IHeaderCtrl2::SetColumnFilter, SetColumnFilter, SetColumnFilter method [MMC], SetColumnFilter method [MMC],IHeaderCtrl2 interface, _slate_iheaderctrl2_setcolumnfilter, mmc.iheaderctrl2_setcolumnfilter, mmc/IHeaderCtrl2::SetColumnFilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IHeaderCtrl2.SetColumnFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IHeaderCtrl2::SetColumnFilter


## -description


The <b>IHeaderCtrl2::SetColumnFilter</b> sets the filter value and its maximum character length for a specified column in a filtered list.


## -parameters




### -param nColumn [in]

A zero-based index that identifies the column for which the filter value and its maximum character length are to be set.


### -param dwType [in]

Filter type to apply to the specified column, taken from the 
<a href="https://msdn.microsoft.com/69e6952c-baea-42ac-9700-1f9a4b8d5e67">MMC_FILTER_TYPE</a> enumeration.


### -param pFilterData [in]

A pointer to an 
<a href="https://msdn.microsoft.com/312d27b8-cfca-48fd-8d39-b0f504421d2d">MMC_FILTERDATA</a> structure that holds the actual filter data.


## -returns



This method can return one of these values.




## -remarks



For both setting and reading filter values, the snap-in owns the 
<a href="https://msdn.microsoft.com/312d27b8-cfca-48fd-8d39-b0f504421d2d">MMC_FILTERDATA</a> structure and any text buffer.

If the snap-in does not explicitly set the filter data for a column in a filtered list by calling <b>IHeaderCtrl2::SetColumnFilter</b>, the filter type defaults to MMC_STRING_FILTER with no default value for the filter (MMC_FILTER_NOVALUE). The default length of the filter is not documented by the Win32 header control, but it is of sufficient length for most likely user inputs. If the snap-in requires a specific length, it should call <b>IHeaderCtrl2::SetColumnFilter</b>.




## -see-also




<a href="https://msdn.microsoft.com/fecf38be-6f45-45ea-a689-ff37b2b92922">IHeaderCtrl2</a>
 

 

