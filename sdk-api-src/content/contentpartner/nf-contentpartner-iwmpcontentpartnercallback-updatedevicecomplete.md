---
UID: NF:contentpartner.IWMPContentPartnerCallback.UpdateDeviceComplete
title: IWMPContentPartnerCallback::UpdateDeviceComplete
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartnercallback_updatedevicecomplete.htm
old-project: WMP
ms.assetid: 0d21d9a0-1a7c-4f4e-9c9d-36a0d30ea63f
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],UpdateDeviceComplete method, IWMPContentPartnerCallback.UpdateDeviceComplete, IWMPContentPartnerCallback::UpdateDeviceComplete, IWMPContentPartnerCallbackUpdateDeviceComplete, UpdateDeviceComplete, UpdateDeviceComplete method [Windows Media Player], UpdateDeviceComplete method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::UpdateDeviceComplete, wmp.iwmpcontentpartnercallback_updatedevicecomplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WMPTransactionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartnerCallback.UpdateDeviceComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartnerCallback::UpdateDeviceComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>UpdateDeviceComplete</b> method notifies Windows Media Player that the online store has finished processing a call to <a href="https://msdn.microsoft.com/893beb65-048f-4496-88e6-b0e0b8db0205">IWMPContentPartner::UpdateDevice</a>.




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




<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 

