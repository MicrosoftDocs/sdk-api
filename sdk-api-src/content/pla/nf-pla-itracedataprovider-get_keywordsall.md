---
UID: NF:pla.ITraceDataProvider.get_KeywordsAll
title: ITraceDataProvider::get_KeywordsAll (pla.h)
description: Retrieves the list of keywords that restricts the category of events that you want the provider to write.
helpviewer_keywords: ["ITraceDataProvider interface [PLA]","KeywordsAll property","ITraceDataProvider.KeywordsAll","ITraceDataProvider.get_KeywordsAll","ITraceDataProvider::KeywordsAll","ITraceDataProvider::get_KeywordsAll","KeywordsAll property [PLA]","KeywordsAll property [PLA]","ITraceDataProvider interface","get_KeywordsAll","pla.itracedataprovider_keywordsall","pla/ITraceDataProvider::KeywordsAll","pla/ITraceDataProvider::get_KeywordsAll"]
old-location: pla\itracedataprovider_keywordsall.htm
tech.root: PLA
ms.assetid: 9ff48234-927b-4b87-a9b8-2a1047b5e3de
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider interface [PLA],KeywordsAll property, ITraceDataProvider.KeywordsAll, ITraceDataProvider.get_KeywordsAll, ITraceDataProvider::KeywordsAll, ITraceDataProvider::get_KeywordsAll, KeywordsAll property [PLA], KeywordsAll property [PLA],ITraceDataProvider interface, get_KeywordsAll, pla.itracedataprovider_keywordsall, pla/ITraceDataProvider::KeywordsAll, pla/ITraceDataProvider::get_KeywordsAll
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
 - ITraceDataProvider::get_KeywordsAll
 - pla/ITraceDataProvider::get_KeywordsAll
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
 - ITraceDataProvider.KeywordsAll
 - ITraceDataProvider.get_KeywordsAll
---

# ITraceDataProvider::get_KeywordsAll


## -description

Retrieves the list of keywords that restricts the category of events that you want the provider to write. The restrictions are in addition to those provided by the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">ITraceDataProvider::KeywordsAny</a> property.

This property is read-only.

## -parameters

## -remarks

The provider writes an event if any of the event's keyword bits match any of the bits set in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">KeywordsAny</a> property. 
The keywords specified in the  <b>KeywordsAll</b> property further restrict the category of events that you want the provider to write. If the event's keyword meets the <b>KeywordsAny</b> condition, the provider will write the event only if all of the bits in the <b>KeywordsAll</b> mask exist in the event's keyword. The <b>KeywordsAll</b> mask is not used if <b>KeywordsAny</b> is zero.

For more information about how the <b>KeywordsAll</b> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">KeywordsAny</a> conditions relate, see the Remarks section of <a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">KeywordsAny</a>.

You use the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface to retrieve or set the keywords value. You can use the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property to retrieve the keywords value (the value of all of the items in the map when combined with the <b>OR</b> operator), or you can enumerate each item in the map to retrieve the individual keyword values.

Likewise, when you set the keywords value, you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property to set the keywords value, or you can call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-add">IValueMap::Add</a> method to add each individual keyword value.

If you use <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> to set the keywords and the value map contains one or more items, PLA searches the collection for matching values and enables them and disables the others. If the value does not exist in the list, PLA adds the keyword (the item is not named).

The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the string representation of the keyword. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the keyword value. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_enabled">IValueMapItem::Enabled</a> property indicates if the keyword is enabled.  You need to use <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface only when you want to name the keyword or you want to enable or disable keywords without having to add or remove them.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">ITraceDataProvider::KeywordsAny</a>