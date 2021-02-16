---
UID: NF:upnp.IUPnPDescriptionDocument.Load
title: IUPnPDescriptionDocument::Load (upnp.h)
description: The Load method loads a document synchronously. This method does not return control to the caller until the load operation is complete.
helpviewer_keywords: ["IUPnPDescriptionDocument interface [UPnP APIs]","Load method","IUPnPDescriptionDocument.Load","IUPnPDescriptionDocument::Load","Load","Load method [UPnP APIs]","Load method [UPnP APIs]","IUPnPDescriptionDocument interface","_upnp_iupnpdescriptiondocument_load","upnp.iupnpdescriptiondocument_load","upnp/IUPnPDescriptionDocument::Load"]
old-location: upnp\iupnpdescriptiondocument_load.htm
tech.root: upnp
ms.assetid: 02ae8af2-44f2-4b7c-a426-f2a26c43da37
ms.date: 12/05/2018
ms.keywords: IUPnPDescriptionDocument interface [UPnP APIs],Load method, IUPnPDescriptionDocument.Load, IUPnPDescriptionDocument::Load, Load, Load method [UPnP APIs], Load method [UPnP APIs],IUPnPDescriptionDocument interface, _upnp_iupnpdescriptiondocument_load, upnp.iupnpdescriptiondocument_load, upnp/IUPnPDescriptionDocument::Load
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
 - IUPnPDescriptionDocument::Load
 - upnp/IUPnPDescriptionDocument::Load
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
 - IUPnPDescriptionDocument.Load
---

# IUPnPDescriptionDocument::Load


## -description

The 
<b>Load</b> method loads a document synchronously. This method does not return control to the caller until the load operation is complete.

## -parameters

### -param bstrUrl [in]

Specifies the URL of the document to load.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h, or one of the following UPnP return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
XML document does not have a device element. It is missing either from the root element or the DeviceList element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPnP_E_DEVICE_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There is no Device element in the specified description document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
XML document is missing one of the required elements from the Device element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ICON_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
XML document does not have an icon element. It is missing from the IconList element, or the DeviceList element does not contain an IconList element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPnP_E_ICON_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There is no Icon element in the specified description document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ICON_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
XML document is missing one of the required elements from the Icon element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPnP_E_ICON_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
There is no Icon Node in the specified description document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ROOT_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
XML document does not have a root element at the top level of the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPnP_E_ROOT_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There is no Root element in the specified description document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_SERVICE_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
XML document does not have a service element. It is missing from the ServiceList element, or the DeviceList element does not contain a ServiceList element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_SERVICE_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
XML document is missing one of the required elements from the Service element.

</td>
</tr>
</table>

## -remarks

This method should not be called from a user interface thread because it can take a long time for the method to return.

If the 
<b>Load</b> method is called by a script within a Web page, <i>bstrUrl</i> may be a relative URL. The address of the current web page is used as the base URL.

If this method is called from a Web page, the URL the caller specifies must refer to the same server from which the Web page was loaded.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>