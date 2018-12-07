---
UID: NF:wmp.IWMPControls.get_currentPosition
title: IWMPControls::get_currentPosition
author: windows-sdk-content
description: The get_currentPosition method retrieves the current position in the media item in seconds from the beginning.
old-location: wmp\iwmpcontrols_get_currentposition.htm
tech.root: WMP
ms.assetid: ba7d42b4-2025-4881-b1eb-98636bb1c5ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPControls interface [Windows Media Player],get_currentPosition method, IWMPControls.get_currentPosition, IWMPControls::get_currentPosition, IWMPControlsget_currentPosition, get_currentPosition, get_currentPosition method [Windows Media Player], get_currentPosition method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_currentposition, wmp/IWMPControls::get_currentPosition
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
 - IWMPControls.get_currentPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls::get_currentPosition


## -description



The <b>get_currentPosition</b> method retrieves the current position in the media item in seconds from the beginning.




## -parameters




### -param pdCurrentPosition [out]

Pointer to a <b>double</b> containing the current position.


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



<a href="https://msdn.microsoft.com/8843852b-f98a-469f-8541-44b3c51ebd6c">IWMPControls::get_currentPositionString</a>



<a href="https://msdn.microsoft.com/7deedeed-8ce9-4fd7-9825-817204a9cb3e">IWMPControls::put_currentPosition</a>
 

 

