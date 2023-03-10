---
UID: NF:pla.ITraceDataProvider.get_Level
title: ITraceDataProvider::get_Level (pla.h)
description: Retrieves the level of information used to enable the provider.
helpviewer_keywords: ["ITraceDataProvider interface [PLA]","Level property","ITraceDataProvider.Level","ITraceDataProvider.get_Level","ITraceDataProvider::Level","ITraceDataProvider::get_Level","Level property [PLA]","Level property [PLA]","ITraceDataProvider interface","base.itracedataprovider_level","get_Level","pla.itracedataprovider_level","pla/ITraceDataProvider::Level","pla/ITraceDataProvider::get_Level"]
old-location: pla\itracedataprovider_level.htm
tech.root: PLA
ms.assetid: 5e9390c4-12d4-4087-b4c8-5f58c2522a93
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider interface [PLA],Level property, ITraceDataProvider.Level, ITraceDataProvider.get_Level, ITraceDataProvider::Level, ITraceDataProvider::get_Level, Level property [PLA], Level property [PLA],ITraceDataProvider interface, base.itracedataprovider_level, get_Level, pla.itracedataprovider_level, pla/ITraceDataProvider::Level, pla/ITraceDataProvider::get_Level
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITraceDataProvider::get_Level
 - pla/ITraceDataProvider::get_Level
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataProvider.Level
 - ITraceDataProvider.get_Level
---

# ITraceDataProvider::get_Level


## -description

Retrieves the level of information used to enable the provider.

This property is read-only.

## -parameters

## -remarks

The <i>ppLevel</i> parameter is a provider-defined value that specifies the level of information that the event generates. For example, you can use this value to indicate the severity level of the events (informational, warning, error) that you want the provider to generate.

You use the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface to retrieve or set the level value. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property contains the level value. 

You can also use the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-add">IValueMap::Add</a> method to add one or more level values. You need to use the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface only when you want to name the level, or you want to enable or disable levels without having to add or remove them. Only one level can be enabled.

The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the string representation of the level, for example, Information. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the level value. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_enabled">IValueMapItem::Enabled</a> property indicates whether the level is enabled.  

If you use <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> to set the level and the value map collection contains one or more items, PLA searches the collection for a matching value and enables it and disables the others. If the value does not exist in the list, PLA adds the level (the item is not named).

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>