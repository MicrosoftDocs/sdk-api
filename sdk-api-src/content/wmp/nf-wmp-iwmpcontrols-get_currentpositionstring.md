---
UID: NF:wmp.IWMPControls.get_currentPositionString
title: IWMPControls::get_currentPositionString
author: windows-sdk-content
description: The get_currentPositionString method retrieves the current position in the media item as a BSTR formatted as HH:MM:SS (hours, minutes, and seconds).
old-location: wmp\iwmpcontrols_get_currentpositionstring.htm
tech.root: WMP
ms.assetid: 8843852b-f98a-469f-8541-44b3c51ebd6c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPControls interface [Windows Media Player],get_currentPositionString method, IWMPControls.get_currentPositionString, IWMPControls::get_currentPositionString, IWMPControlsget_currentPositionString, get_currentPositionString, get_currentPositionString method [Windows Media Player], get_currentPositionString method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_currentpositionstring, wmp/IWMPControls::get_currentPositionString
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
 - IWMPControls.get_currentPositionString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls::get_currentPositionString


## -description



The <b>get_currentPositionString</b> method retrieves the current position in the media item as a <b>BSTR</b> formatted as HH:MM:SS (hours, minutes, and seconds).




## -parameters




### -param pbstrCurrentPosition [out]

Pointer to a <b>BSTR</b> containing the current position.


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



If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/ba7d42b4-2025-4881-b1eb-98636bb1c5ce">IWMPControls::get_currentPosition</a>
 

 

