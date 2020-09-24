---
UID: NF:upnp.IUPnPDescriptionDocumentCallback.LoadComplete
title: IUPnPDescriptionDocumentCallback::LoadComplete (upnp.h)
description: The LoadComplete method is invoked when the UPnP framework has finished loading a device description.
helpviewer_keywords: ["IUPnPDescriptionDocumentCallback interface [UPnP APIs]","LoadComplete method","IUPnPDescriptionDocumentCallback.LoadComplete","IUPnPDescriptionDocumentCallback::LoadComplete","LoadComplete","LoadComplete method [UPnP APIs]","LoadComplete method [UPnP APIs]","IUPnPDescriptionDocumentCallback interface","UPNP_E_DEVICE_ELEMENT_EXPECTED","UPNP_E_DEVICE_NODE_INCOMPLETE","UPNP_E_ICON_ELEMENT_EXPECTED","UPNP_E_ICON_NODE_INCOMPLETE","UPNP_E_ROOT_ELEMENT_EXPECTED","UPNP_E_SERVICE_ELEMENT_EXPECTED","UPNP_E_SERVICE_NODE_INCOMPLETE","_upnp_iupnpdescriptiondocumentcallback_loadcomplete","upnp.iupnpdescriptiondocumentcallback_loadcomplete","upnp/IUPnPDescriptionDocumentCallback::LoadComplete"]
old-location: upnp\iupnpdescriptiondocumentcallback_loadcomplete.htm
tech.root: upnp
ms.assetid: 899b1aa4-597c-4434-80cc-2ea22759fbc8
ms.date: 12/05/2018
ms.keywords: IUPnPDescriptionDocumentCallback interface [UPnP APIs],LoadComplete method, IUPnPDescriptionDocumentCallback.LoadComplete, IUPnPDescriptionDocumentCallback::LoadComplete, LoadComplete, LoadComplete method [UPnP APIs], LoadComplete method [UPnP APIs],IUPnPDescriptionDocumentCallback interface, UPNP_E_DEVICE_ELEMENT_EXPECTED, UPNP_E_DEVICE_NODE_INCOMPLETE, UPNP_E_ICON_ELEMENT_EXPECTED, UPNP_E_ICON_NODE_INCOMPLETE, UPNP_E_ROOT_ELEMENT_EXPECTED, UPNP_E_SERVICE_ELEMENT_EXPECTED, UPNP_E_SERVICE_NODE_INCOMPLETE, _upnp_iupnpdescriptiondocumentcallback_loadcomplete, upnp.iupnpdescriptiondocumentcallback_loadcomplete, upnp/IUPnPDescriptionDocumentCallback::LoadComplete
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDescriptionDocumentCallback::LoadComplete
 - upnp/IUPnPDescriptionDocumentCallback::LoadComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocumentCallback.LoadComplete
---

# IUPnPDescriptionDocumentCallback::LoadComplete


## -description

The 
<b>LoadComplete</b> method is invoked when the UPnP framework has finished loading a device description.

## -parameters

### -param hrLoadResult [in]

Specifies the load operation that the UPnP framework has completed. Possible return values are:

<table>
<tr>
<th>UPnP-specific return value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UPNP_E_DEVICE_ELEMENT_EXPECTED"></a><a id="upnp_e_device_element_expected"></a><dl>
<dt><b>UPNP_E_DEVICE_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have a device element. It is missing either from the root element or the <b>DeviceList</b> element.

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_E_DEVICE_NODE_INCOMPLETE"></a><a id="upnp_e_device_node_incomplete"></a><dl>
<dt><b>UPNP_E_DEVICE_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The XML document is missing one of the required elements from the <b>Device</b> element.

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_E_ICON_ELEMENT_EXPECTED"></a><a id="upnp_e_icon_element_expected"></a><dl>
<dt><b>UPNP_E_ICON_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have an icon element. It is missing from the <b>IconList</b> element, or the <b>DeviceList</b> element does not contain an <b>IconList</b> element.

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_E_ICON_NODE_INCOMPLETE"></a><a id="upnp_e_icon_node_incomplete"></a><dl>
<dt><b>UPNP_E_ICON_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The XML document is missing one of the required elements from the <b>Icon</b> element.

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_E_ROOT_ELEMENT_EXPECTED"></a><a id="upnp_e_root_element_expected"></a><dl>
<dt><b>UPNP_E_ROOT_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have a root element at the top level of the document.

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_E_SERVICE_ELEMENT_EXPECTED"></a><a id="upnp_e_service_element_expected"></a><dl>
<dt><b>UPNP_E_SERVICE_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have a service element. It is missing from the <b>ServiceList</b> element, or the <b>DeviceList</b> element does not contain a <b>ServiceList</b> element.

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_E_SERVICE_NODE_INCOMPLETE"></a><a id="upnp_e_service_node_incomplete"></a><dl>
<dt><b>UPNP_E_SERVICE_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The XML document is missing one of the required elements from the <b>Service</b> element.

</td>
</tr>
</table>

## -returns

The application should return S_OK.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocumentcallback">IUPnPDescriptionDocumentCallback</a>