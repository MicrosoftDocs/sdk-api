---
UID: NF:contentpartner.IWMPContentPartnerCallback.UpdateDeviceComplete
title: IWMPContentPartnerCallback::UpdateDeviceComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.helpviewer_keywords: ["IWMPContentPartnerCallback interface [Windows Media Player]","UpdateDeviceComplete method","IWMPContentPartnerCallback.UpdateDeviceComplete","IWMPContentPartnerCallback::UpdateDeviceComplete","IWMPContentPartnerCallbackUpdateDeviceComplete","UpdateDeviceComplete","UpdateDeviceComplete method [Windows Media Player]","UpdateDeviceComplete method [Windows Media Player]","IWMPContentPartnerCallback interface","contentpartner/IWMPContentPartnerCallback::UpdateDeviceComplete","wmp.iwmpcontentpartnercallback_updatedevicecomplete"]
old-location: wmp\iwmpcontentpartnercallback_updatedevicecomplete.htm
tech.root: WMP
ms.assetid: 0d21d9a0-1a7c-4f4e-9c9d-36a0d30ea63f
ms.date: 12/05/2018
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],UpdateDeviceComplete method, IWMPContentPartnerCallback.UpdateDeviceComplete, IWMPContentPartnerCallback::UpdateDeviceComplete, IWMPContentPartnerCallbackUpdateDeviceComplete, UpdateDeviceComplete, UpdateDeviceComplete method [Windows Media Player], UpdateDeviceComplete method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::UpdateDeviceComplete, wmp.iwmpcontentpartnercallback_updatedevicecomplete
f1_keywords:
- contentpartner/IWMPContentPartnerCallback.UpdateDeviceComplete
dev_langs:
- c++
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- contentpartner.h
api_name:
- IWMPContentPartnerCallback.UpdateDeviceComplete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartnerCallback::UpdateDeviceComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>UpdateDeviceComplete</b> method notifies Windows Media Player that the online store has finished processing a call to <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice">IWMPContentPartner::UpdateDevice</a>.




## -parameters




### -param bstrDeviceName [in]

String containing the device name.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method should be called in response to <b>UpdateDevice</b>, following the completion of the device update.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>
 

 

