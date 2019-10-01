---
UID: NF:mswmdm.ISCPSecureExchange3.TransferCompleteForDevice
title: ISCPSecureExchange3::TransferCompleteForDevice (mswmdm.h)
author: windows-sdk-content
description: The TransferCompleteForDevice method is called by Windows Media Device Manager to signal the end of a data transfer for a specific device.
old-location: wmdm\iscpsecureexchange3__transfercompletefordevice.htm
tech.root: WMDM
ms.assetid: 5144d290-444d-4a8c-ad3d-292bb8168e99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISCPSecureExchange3 interface [windows Media Device Manager],TransferCompleteForDevice method, ISCPSecureExchange3.TransferCompleteForDevice, ISCPSecureExchange3::TransferCompleteForDevice, ISCPSecureExchange3TransferCompleteForDevice, TransferCompleteForDevice, TransferCompleteForDevice method [windows Media Device Manager], TransferCompleteForDevice method [windows Media Device Manager],ISCPSecureExchange3 interface, mswmdm/ISCPSecureExchange3::TransferCompleteForDevice, wmdm.iscpsecureexchange3__transfercompletefordevice
ms.topic: method
f1_keywords: 
 - "mswmdm/ISCPSecureExchange3.TransferCompleteForDevice"
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - ISCPSecureExchange3.TransferCompleteForDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCPSecureExchange3::TransferCompleteForDevice


## -description


The <b>TransferCompleteForDevice</b> method is called by Windows Media Device Manager to signal the end of a data transfer for a specific device.


## -parameters




### -param pDevice

Pointer to a device object.


## -returns



If the method succeeds, it returns S_OK. If the method fails, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOT_CERTIFIED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not authorized to use this interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NORIGHTS</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the rights required to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_MAC_CHECK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The message authentication code is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



This method is identical to <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercomplete">ISCPSecureExchange::TransferComplete</a> except that this method is called when transfer is completed within a transfer session.

In that case, the secure content provider needs to know which device the transfer was completed for, so this method accepts a <i>pDevice</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3">ISCPSecureExchange3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-transfercomplete">ISCPSecureExchange::TransferComplete</a>
 

 

