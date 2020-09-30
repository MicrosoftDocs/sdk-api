---
UID: NF:wsddisco.IWSDiscoveredService.GetExtendedDiscoXML
title: IWSDiscoveredService::GetExtendedDiscoXML (wsddisco.h)
description: Retrieves custom or extensible data provided in the header or body of the SOAP message.
helpviewer_keywords: ["GetExtendedDiscoXML","GetExtendedDiscoXML method","GetExtendedDiscoXML method","IWSDiscoveredService interface","IWSDiscoveredService interface","GetExtendedDiscoXML method","IWSDiscoveredService.GetExtendedDiscoXML","IWSDiscoveredService::GetExtendedDiscoXML","ncd.iwsdiscoveredservice_getextendeddiscoxml","wsddisco/IWSDiscoveredService::GetExtendedDiscoXML"]
old-location: ncd\iwsdiscoveredservice_getextendeddiscoxml.htm
tech.root: ncd
ms.assetid: 6ca12b1b-4adf-4c54-90b5-ab5286af9252
ms.date: 12/05/2018
ms.keywords: GetExtendedDiscoXML, GetExtendedDiscoXML method, GetExtendedDiscoXML method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetExtendedDiscoXML method, IWSDiscoveredService.GetExtendedDiscoXML, IWSDiscoveredService::GetExtendedDiscoXML, ncd.iwsdiscoveredservice_getextendeddiscoxml, wsddisco/IWSDiscoveredService::GetExtendedDiscoXML
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDiscoveredService::GetExtendedDiscoXML
 - wsddisco/IWSDiscoveredService::GetExtendedDiscoXML
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveredService.GetExtendedDiscoXML
---

# IWSDiscoveredService::GetExtendedDiscoXML


## -description

Retrieves custom or extensible data provided in the header or body of the SOAP message.

## -parameters

### -param ppHeaderAny [out]

Custom data added to the header portion of the SOAP message. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>. Do not deallocate the output structure.

### -param ppBodyAny [out]

Custom data added to the body portion of the SOAP message. For details, see <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a>. Do not deallocate the output structure.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
</table>

## -remarks

Some devices may add custom data to the header and body portions of the SOAP message to convey additional information in the discovery phase.

The resulting pointer values are  only valid for the lifetime of the <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> object.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>