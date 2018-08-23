---
UID: NF:upnp.IUPnPServiceEnumProperty.SetServiceEnumProperty
title: IUPnPServiceEnumProperty::SetServiceEnumProperty
author: windows-sdk-content
description: The SetServiceEnumProperty method is used to indicate opt-in to the delayed Service Control Protocol Description (SCPD) download and event subscription for the IUPnPService objects enumerated from the IUPnPServices object.
old-location: upnp\iupnpserviceenumproperty_setserviceenumproperty.htm
old-project: upnp
ms.assetid: B138A230-7523-4803-ACE8-4F636DD54D86
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: IUPnPServiceEnumProperty interface [UPnP APIs],SetServiceEnumProperty method, IUPnPServiceEnumProperty.SetServiceEnumProperty, IUPnPServiceEnumProperty::SetServiceEnumProperty, SetServiceEnumProperty, SetServiceEnumProperty method [UPnP APIs], SetServiceEnumProperty method [UPnP APIs],IUPnPServiceEnumProperty interface, upnp.iupnpserviceenumproperty_setserviceenumproperty, upnp/IUPnPServiceEnumProperty::SetServiceEnumProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceEnumProperty.SetServiceEnumProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceEnumProperty::SetServiceEnumProperty


## -description


The <b>SetServiceEnumProperty</b> method is used to indicate opt-in to the delayed Service Control Protocol Description (SCPD) download and event subscription for the <a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a> objects enumerated from the <a href="https://msdn.microsoft.com/8d5e487f-d2d4-4603-918c-e751d698be3c">IUPnPServices</a> object.


## -parameters




### -param dwMask






#### - dwMASK

Specifies a bit-wise flag to indicate an opt-in to the delayed SCPD download and even subscription. Possible values include:

<table>
<tr>
<th>Flag</th>
<th>Value</th>
</tr>
<tr>
<td>UPNP_SERVICE_DELAY_SCPD_AND_SUBSCRIPTION</td>
<td>0x1</td>
</tr>
</table>
 


## -returns



Returns <b>S_OK</b> on success. Otherwise, this method returns <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/B63CCE08-548F-44D3-BAE3-84E4358F25AD">IUPnPServiceEnumProperty</a>
 

 

