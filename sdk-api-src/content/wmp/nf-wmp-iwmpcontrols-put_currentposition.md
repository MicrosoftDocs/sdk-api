---
UID: NF:wmp.IWMPControls.put_currentPosition
title: IWMPControls::put_currentPosition
author: windows-sdk-content
description: The put_currentPosition method specifies the current position in the media item in seconds from the beginning.
old-location: wmp\iwmpcontrols_put_currentposition.htm
old-project: WMP
ms.assetid: 7deedeed-8ce9-4fd7-9825-817204a9cb3e
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPControls interface [Windows Media Player],put_currentPosition method, IWMPControls.put_currentPosition, IWMPControls::put_currentPosition, IWMPControlsput_currentPosition, put_currentPosition, put_currentPosition method [Windows Media Player], put_currentPosition method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_put_currentposition, wmp/IWMPControls::put_currentPosition
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPControls.put_currentPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls::put_currentPosition


## -description



The <b>put_currentPosition</b> method specifies the current position in the media item in seconds from the beginning.




## -parameters




### -param dCurrentPosition [in]

<b>double</b> containing the current position.


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
 




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/ba7d42b4-2025-4881-b1eb-98636bb1c5ce">IWMPControls::get_currentPosition</a>
 

 

