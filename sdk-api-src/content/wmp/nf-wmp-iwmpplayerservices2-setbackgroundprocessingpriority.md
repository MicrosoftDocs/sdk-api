---
UID: NF:wmp.IWMPPlayerServices2.setBackgroundProcessingPriority
title: IWMPPlayerServices2::setBackgroundProcessingPriority method
author: windows-driver-content
description: The setBackgroundProcessingPriority method specifies a priority level for general background processing tasks.
old-location: wmp\iwmpplayerservices2_setbackgroundprocessingpriority.htm
old-project: WMP
ms.assetid: 1e3536d2-006b-4019-a9c5-c460135cf555
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPPlayerServices2, IWMPPlayerServices2 interface [Windows Media Player], setBackgroundProcessingPriority method, IWMPPlayerServices2::setBackgroundProcessingPriority, IWMPPlayerServices2setBackgroundProcessingPriority, setBackgroundProcessingPriority method [Windows Media Player], setBackgroundProcessingPriority method [Windows Media Player], IWMPPlayerServices2 interface, setBackgroundProcessingPriority,IWMPPlayerServices2.setBackgroundProcessingPriority, wmp.iwmpplayerservices2_setbackgroundprocessingpriority, wmp/IWMPPlayerServices2::setBackgroundProcessingPriority
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPPlayerServices2.setBackgroundProcessingPriority
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayerServices2::setBackgroundProcessingPriority method


## -description



The <b>setBackgroundProcessingPriority</b> method specifies a priority level for general background processing tasks.




## -parameters




### -param bstrPriority [in]

<b>BSTR</b> containing one of the following values: "High", "Normal", "Off", or "Urgent".


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>
 




## -remarks



This method is used only when remoting the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/abbce425-9185-4235-8d8e-28be591be8e5">IWMPPlayerServices2 Interface</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

