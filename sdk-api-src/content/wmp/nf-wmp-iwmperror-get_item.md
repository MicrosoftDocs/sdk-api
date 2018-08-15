---
UID: NF:wmp.IWMPError.get_item
title: IWMPError::get_item
author: windows-sdk-content
description: The get_item method retrieves a pointer to an IWMPErrorItem interface from the error queue.
old-location: wmp\iwmperror_get_item.htm
old-project: WMP
ms.assetid: 6fda2f53-e8d8-4b67-9aa1-72273fc68f6c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPError interface [Windows Media Player],get_item method, IWMPError.get_item, IWMPError::get_item, IWMPErrorget_item, get_item, get_item method [Windows Media Player], get_item method [Windows Media Player],IWMPError interface, wmp.iwmperror_get_item, wmp/IWMPError::get_item
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
 - IWMPError.get_item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPError::get_item


## -description



The <b>get_item</b> method retrieves a pointer to an <b>IWMPErrorItem</b> interface from the error queue.




## -parameters




### -param dwIndex [in]

<b>long</b> containing the index of the pointer to an <b>IWMPErrorItem</b> interface.


### -param ppErrorItem [out]

Pointer to a pointer to an <b>IWMPErrorItem</b> interface.


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



Windows Media Player can generate a number of errors in response to an error condition. This method retrieves a specific error in the queue by using an index number. The index numbers for the error queue begin with zero.

You should set a <b>VARIANT_BOOL</b> to <b>FALSE</b> and pass it into <b>IWMPSettings::put_enableErrorDialogs</b> if you choose to display custom error messages.




## -see-also




<a href="https://msdn.microsoft.com/f22759cd-0ca7-4992-bb17-0272b35d6d75">IWMPError Interface</a>



<a href="https://msdn.microsoft.com/4675eebf-80d7-4412-b3f1-ec54b977db31">IWMPErrorItem Interface</a>
 

 

