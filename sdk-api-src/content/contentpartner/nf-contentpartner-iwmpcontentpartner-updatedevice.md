---
UID: NF:contentpartner.IWMPContentPartner.UpdateDevice
title: IWMPContentPartner::UpdateDevice
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner_updatedevice.htm
tech.root: WMP
ms.assetid: 893beb65-048f-4496-88e6-b0e0b8db0205
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],UpdateDevice method, IWMPContentPartner.UpdateDevice, IWMPContentPartner::UpdateDevice, IWMPContentPartnerUpdateDevice, UpdateDevice, UpdateDevice method [Windows Media Player], UpdateDevice method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::UpdateDevice, wmp.iwmpcontentpartner_updatedevice
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMPContentPartner.UpdateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPContentPartner::UpdateDevice


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>UpdateDevice</b> method notifies the content partner plug-in that a portable device is being synchronized.




## -parameters




### -param bstrDeviceName [in]

<b>BSTR</b> containing the device name.


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



You must call <a href="https://msdn.microsoft.com/en-us/library/Dd563154(v=VS.85).aspx">IWMPContentPartnerCallback::UpdateDeviceComplete</a> exactly once for each call to <b>UpdateDevice</b> from which you return a success code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563141(v=VS.85).aspx">IWMPContentPartner Interface</a>
 

 

