---
UID: NF:wmp.IWMPErrorItem2.get_condition
title: IWMPErrorItem2::get_condition
author: windows-sdk-content
description: The get_condition method retrieves a value indicating the condition for the error.
old-location: wmp\iwmperroritem2_get_condition.htm
old-project: WMP
ms.assetid: fe72bb1c-78ac-4a10-9abf-81722139d842
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPErrorItem2 interface [Windows Media Player],get_condition method, IWMPErrorItem2.get_condition, IWMPErrorItem2::get_condition, IWMPErrorItem2get_condition, get_condition, get_condition method [Windows Media Player], get_condition method [Windows Media Player],IWMPErrorItem2 interface, wmp.iwmperroritem2_get_condition, wmp/IWMPErrorItem2::get_condition
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
 - IWMPErrorItem2.get_condition
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPErrorItem2::get_condition


## -description



The <b>get_condition</b> method retrieves a value indicating the condition for the error.




## -parameters




### -param plCondition [out]

Pointer to a <b>long</b> containing the condition code.


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



The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.




## -see-also




<a href="https://msdn.microsoft.com/b71d06db-c9bc-44fc-9e23-a16f89c56c1c">IWMPErrorItem2 Interface</a>
 

 

