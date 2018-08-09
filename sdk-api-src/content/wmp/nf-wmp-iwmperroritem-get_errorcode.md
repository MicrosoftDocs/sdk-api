---
UID: NF:wmp.IWMPErrorItem.get_errorCode
title: IWMPErrorItem::get_errorCode
author: windows-sdk-content
description: The get_errorCode method retrieves the current error code.
old-location: wmp\iwmperroritem_get_errorcode.htm
old-project: WMP
ms.assetid: e809a1bf-1c7e-4006-9d27-e9921f2f14b2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_errorCode method, IWMPErrorItem.get_errorCode, IWMPErrorItem::get_errorCode, IWMPErrorItemget_errorCode, get_errorCode, get_errorCode method [Windows Media Player], get_errorCode method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_errorcode, wmp/IWMPErrorItem::get_errorCode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPErrorItem.get_errorCode
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPErrorItem::get_errorCode


## -description



The <b>get_errorCode</b> method retrieves the current error code.




## -parameters




### -param phr [out]

Pointer to a <b>long</b> containing the error code.


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



You should set a <b>VARIANT_BOOL</b> to <b>FALSE</b> and pass it into <b>IWMPSettings::put_enableErrorDialogs</b> if you choose to display custom error messages.




## -see-also




<a href="https://msdn.microsoft.com/4675eebf-80d7-4412-b3f1-ec54b977db31">IWMPErrorItem Interface</a>



<a href="https://msdn.microsoft.com/c2a0e2bf-d0e4-4b2c-a8d4-15bae4214393">IWMPSettings::put_enableErrorDialogs</a>
 

 

