---
UID: NF:wmp.IWMPSyncDevice.stop
title: IWMPSyncDevice::stop (wmp.h)
description: The stop method ends synchronization.
helpviewer_keywords: ["IWMPSyncDevice interface [Windows Media Player]","stop method","IWMPSyncDevice.stop","IWMPSyncDevice::stop","IWMPSyncDevicestop","stop","stop method [Windows Media Player]","stop method [Windows Media Player]","IWMPSyncDevice interface","wmp.iwmpsyncdevice_stop","wmp/IWMPSyncDevice::stop"]
old-location: wmp\iwmpsyncdevice_stop.htm
tech.root: WMP
ms.assetid: 30e6787e-851b-420c-934c-5f8e5e4d83df
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice interface [Windows Media Player],stop method, IWMPSyncDevice.stop, IWMPSyncDevice::stop, IWMPSyncDevicestop, stop, stop method [Windows Media Player], stop method [Windows Media Player],IWMPSyncDevice interface, wmp.iwmpsyncdevice_stop, wmp/IWMPSyncDevice::stop
f1_keywords:
- wmp/IWMPSyncDevice.stop
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPSyncDevice.stop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncDevice::stop


## -description



The <b>stop</b> method ends synchronization.




## -parameters






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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_PDA_INITIALIZINGDEVICES (0xC00D118D)</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Player is currently busy initializing devices. Please try again later.

</td>
</tr>
</table>
 




## -remarks



<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start">IWMPSyncDevice::start</a>
 

 

