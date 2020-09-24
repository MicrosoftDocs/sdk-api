---
UID: NF:pla.ITraceDataProvider.get_Properties
title: ITraceDataProvider::get_Properties (pla.h)
description: Retrieves the list of extended data items that Event Tracing for Windows (ETW) includes with the event.
helpviewer_keywords: ["ITraceDataProvider interface [PLA]","Properties property","ITraceDataProvider.Properties","ITraceDataProvider.get_Properties","ITraceDataProvider::Properties","ITraceDataProvider::get_Properties","Properties property [PLA]","Properties property [PLA]","ITraceDataProvider interface","base.itracedataprovider_properties","get_Properties","pla.itracedataprovider_properties","pla/ITraceDataProvider::Properties","pla/ITraceDataProvider::get_Properties"]
old-location: pla\itracedataprovider_properties.htm
tech.root: PLA
ms.assetid: 1dc21423-fa55-4312-b86a-63d4f59e4cf1
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider interface [PLA],Properties property, ITraceDataProvider.Properties, ITraceDataProvider.get_Properties, ITraceDataProvider::Properties, ITraceDataProvider::get_Properties, Properties property [PLA], Properties property [PLA],ITraceDataProvider interface, base.itracedataprovider_properties, get_Properties, pla.itracedataprovider_properties, pla/ITraceDataProvider::Properties, pla/ITraceDataProvider::get_Properties
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
 - ITraceDataProvider::get_Properties
 - pla/ITraceDataProvider::get_Properties
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
 - ITraceDataProvider.Properties
 - ITraceDataProvider.get_Properties
---

# ITraceDataProvider::get_Properties


## -description

Retrieves the list of extended data items that Event Tracing for Windows (ETW) includes with the event.

This property is read-only.

## -parameters

## -remarks

Use this property to request the following data items with the event.

<table>
<tr>
<th>Data item</th>
<th>Description</th>
</tr>
<tr>
<td>
Sid (value 0x01)

</td>
<td>
Includes the user's security identifier.

</td>
</tr>
<tr>
<td>
SessionId (value 0x02)

</td>
<td>
Includes the session identifier.

</td>
</tr>
<tr>
<td>
StackTrace (value 0x04)

</td>
<td>
Includes the stack trace.

</td>
</tr>
</table>
 

Use the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a> interface to retrieve or specify the extended data items. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemap-get_value">IValueMap::Value</a> property contains items that are combined by using the <b>OR</b> operator. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_key">IValueMapItem::Key</a> property contains the string representation of the extended data item. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ivaluemapitem-get_value">IValueMapItem::Value</a> property contains the extended data item value.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">ITraceDataProvider</a>