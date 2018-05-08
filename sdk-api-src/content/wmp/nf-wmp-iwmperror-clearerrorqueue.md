---
UID: NF:wmp.IWMPError.clearErrorQueue
title: IWMPError::clearErrorQueue
author: windows-driver-content
description: The clearErrorQueue method clears the errors from the error queue.
old-location: wmp\iwmperror_clearerrorqueue.htm
old-project: WMP
ms.assetid: 8c965b48-d178-4b41-add7-0b7d208380a3
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPError interface [Windows Media Player],clearErrorQueue method, IWMPError.clearErrorQueue, IWMPError::clearErrorQueue, IWMPErrorclearErrorQueue, clearErrorQueue, clearErrorQueue method [Windows Media Player], clearErrorQueue method [Windows Media Player],IWMPError interface, wmp.iwmperror_clearerrorqueue, wmp/IWMPError::clearErrorQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPError.clearErrorQueue
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPError::clearErrorQueue


## -description



The <b>clearErrorQueue</b> method clears the errors from the error queue.




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
</table>
 




## -remarks



Use this method to clear the error queue after a series of errors has been processed.

You should set a <b>VARIANT_BOOL</b> to <b>FALSE</b> and pass it into <b>IWMPSettings::put_enableErrorDialogs</b> if you choose to display custom error messages.




## -see-also




<a href="https://msdn.microsoft.com/f22759cd-0ca7-4992-bb17-0272b35d6d75">IWMPError Interface</a>
 

 

