---
UID: NE:mmc._MMC_FILTER_TYPE
title: MMC_FILTER_TYPE (mmc.h)
description: The MMC_FILTER_TYPE enumeration is introduced in MMC 1.2.
helpviewer_keywords: ["MMC_FILTER_NOVALUE","MMC_FILTER_TYPE","MMC_FILTER_TYPE enumeration [MMC]","MMC_INT_FILTER","MMC_STRING_FILTER","_slate_mmc_filter_type","mmc.mmc_filter_type","mmc/MMC_FILTER_NOVALUE","mmc/MMC_FILTER_TYPE","mmc/MMC_INT_FILTER","mmc/MMC_STRING_FILTER"]
old-location: mmc\mmc_filter_type.htm
tech.root: mmc
ms.assetid: 69e6952c-baea-42ac-9700-1f9a4b8d5e67
ms.date: 12/05/2018
ms.keywords: MMC_FILTER_NOVALUE, MMC_FILTER_TYPE, MMC_FILTER_TYPE enumeration [MMC], MMC_INT_FILTER, MMC_STRING_FILTER, _slate_mmc_filter_type, mmc.mmc_filter_type, mmc/MMC_FILTER_NOVALUE, mmc/MMC_FILTER_TYPE, mmc/MMC_INT_FILTER, mmc/MMC_STRING_FILTER
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
req.typenames: MMC_FILTER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_FILTER_TYPE
 - mmc/_MMC_FILTER_TYPE
 - MMC_FILTER_TYPE
 - mmc/MMC_FILTER_TYPE
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
 - MMC_FILTER_TYPE
---

# MMC_FILTER_TYPE enumeration


## -description

The 
<b>MMC_FILTER_TYPE</b> enumeration is introduced in MMC 1.2.

The 
<b>MMC_FILTER_TYPE</b> enumeration defines the filter type that is associated with a filter applied to a column in a filtered list. The values can be used in the <i>dwType</i> parameter of the 
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-setcolumnfilter">IHeaderCtrl2::SetColumnFilter</a> method and the <i>pdwType</i> parameter of the 
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-getcolumnfilter">IHeaderCtrl2::GetColumnFilter</a> method.

## -enum-fields

### -field MMC_STRING_FILTER:0

String filter.

### -field MMC_INT_FILTER:0x1

Integer filter.

### -field MMC_FILTER_NOVALUE:0x8000

When used by the 
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-setcolumnfilter">IHeaderCtrl2::SetColumnFilter</a> method, the snap-in sets the flag to clear the column filter.

When used by the 
<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-getcolumnfilter">IHeaderCtrl2::GetColumnFilter</a> method, the flag is set to indicate that the column filter is empty.

## -remarks

The <b>MMC_FILTER_NOVALUE</b> enumerator value is not a filter type, but a flag that can be OR'd with a filter type. For example, to set a string type filter with no default value, you set the filter type to the following: <code>MMC_STRING_FILTER | MMC_FILTER_NOVALUE</code>.

When reading filter data, if no value has been entered by the snap-in or the user, the return type will be the filter type OR'd with <b>MMC_FILTER_NOVALUE</b>.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-getcolumnfilter">IHeaderCtrl2::GetColumnFilter</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iheaderctrl2-setcolumnfilter">IHeaderCtrl2::SetColumnFilter</a>
