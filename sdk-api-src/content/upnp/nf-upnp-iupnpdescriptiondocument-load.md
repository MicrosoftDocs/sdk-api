---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/25bd3abd-b270-4609-93bb-a786ccaa95dd">IUPnPDescriptionDocument</a>



<a href="https://msdn.microsoft.com/bfb1d833-13e8-4ffe-832d-f6640a42055a">IUPnPDescriptionDocument::LoadAsync</a>
 

 

