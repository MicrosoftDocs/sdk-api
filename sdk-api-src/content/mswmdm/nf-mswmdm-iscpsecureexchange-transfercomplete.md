---
UID: NF:mswmdm.ISCPSecureExchange.TransferComplete
title: ISCPSecureExchange::TransferComplete (mswmdm.h)
author: windows-sdk-content
description: The TransferComplete method is called by Windows Media Device Manager to signal the end of a secure transfer of data. In this method, the secure content provider can perform any additional processing required to enable the content on the target device.
old-location: wmdm\iscpsecureexchange_transfercomplete.htm
tech.root: WMDM
ms.assetid: 8a7a6de0-ab37-4764-8feb-82676e1e62ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISCPSecureExchange interface [windows Media Device Manager],TransferComplete method, ISCPSecureExchange.TransferComplete, ISCPSecureExchange::TransferComplete, ISCPSecureExchangeTransferComplete, TransferComplete, TransferComplete method [windows Media Device Manager], TransferComplete method [windows Media Device Manager],ISCPSecureExchange interface, mswmdm/ISCPSecureExchange::TransferComplete, wmdm.iscpsecureexchange_transfercomplete
ms.topic: method
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
 - ISCPSecureExchange.TransferComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCPSecureExchange::TransferComplete


## -description



The <b>TransferComplete</b> method is called by Windows Media Device Manager to signal the end of a secure transfer of data. In this method, the secure content provider can perform any additional processing required to enable the content on the target device.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

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
 




## -see-also




<a href="https://msdn.microsoft.com/8c61e1a0-18fc-4ae9-881a-0362166012d9">ISCPSecureExchange Interface</a>
 

 

