---
UID: NF:pla.ITraceDataProvider.get_KeywordsAny
title: ITraceDataProvider::get_KeywordsAny (pla.h)
description: Retrieves the list of keywords that determine the category of events that you want the provider to write.
helpviewer_keywords: ["ITraceDataProvider interface [PLA]","KeywordsAny property","ITraceDataProvider.KeywordsAny","ITraceDataProvider.get_KeywordsAny","ITraceDataProvider::KeywordsAny","ITraceDataProvider::get_KeywordsAny","KeywordsAny property [PLA]","KeywordsAny property [PLA]","ITraceDataProvider interface","get_KeywordsAny","pla.itracedataprovider_keywordsany","pla/ITraceDataProvider::KeywordsAny","pla/ITraceDataProvider::get_KeywordsAny"]
old-location: pla\itracedataprovider_keywordsany.htm
tech.root: PLA
ms.assetid: 10159c09-609a-4263-a515-241ab942c3e8
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider interface [PLA],KeywordsAny property, ITraceDataProvider.KeywordsAny, ITraceDataProvider.get_KeywordsAny, ITraceDataProvider::KeywordsAny, ITraceDataProvider::get_KeywordsAny, KeywordsAny property [PLA], KeywordsAny property [PLA],ITraceDataProvider interface, get_KeywordsAny, pla.itracedataprovider_keywordsany, pla/ITraceDataProvider::KeywordsAny, pla/ITraceDataProvider::get_KeywordsAny
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
 - ITraceDataProvider::get_KeywordsAny
 - pla/ITraceDataProvider::get_KeywordsAny
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
 - ITraceDataProvider.KeywordsAny
 - ITraceDataProvider.get_KeywordsAny
---

# ITraceDataProvider::get_KeywordsAny


## -description

Retrieves the list of keywords that determine the category of events that you want the provider to write.

This property is read-only.

## -parameters

## -remarks

Keywords determine the category of events that you want the provider to write. The provider writes an event if any of the event's keyword bits match any of the bits set in this <b>KeywordsAny</b> mask.

To include all events that a provider provides, set this property to zero. To include only specific events, set this keyword mask to those specific events. For example, if the provider defines an event for its initialization and clean-up routines (bit 0), an event for its file operations (bit 1), and an event for its calculation operations (bit 2), you can choose to include only two of these events by setting this mask to 5 (set bits 0 and 2) to receive initialization and clean-up events and calculation events.

To further restrict the category of events that you want the provider to write, also set the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsall">ITraceDataProvider::KeywordsAll</a> property.

If the provider defines more complex event keywords (for example, the provider defines an event that sets bit 0 for read and bit 1 for local access and a second event that sets bit 0 for read and bit 2 for remote access), you could set this mask to 1 to receive all read events, or you could set this mask to 1 and the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsall">KeywordsAll</a> mask to 3 to receive local reads only.

If an event's keyword is zero, the provider will write the event to the session, regardless of this mask or the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsall">KeywordsAll</a> mask.



For providers that were written on an operating system prior to Windows Vista, the keyword value will be mapped to the enable flags.

You use the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface to retrieve or set the keywords value. You can use the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property to retrieve the keywords value (the value of all of the items in the map when combined with the <b>OR</b> operator), or you can enumerate each item in the map to retrieve the individual keyword values.

Likewise, when you set the keywords value, you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property to set the keywords value, or you can call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-add">IValueMap::Add</a> method to add each individual keyword value.

If you use <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> to set the keywords and the value map contains one or more items, PLA searches the collection for matching values and enables them and disables the others. If the value does not exist in the list, PLA adds the keyword (the item is not named).

The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the string representation of the keyword. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the keyword value. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_enabled">IValueMapItem::Enabled</a> property indicates if the keyword is enabled.  You need to use the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface only when you want to name the keyword or you want to enable or disable keywords without having to add or remove them.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsall">ITraceDataProvider::KeywordsAll</a>