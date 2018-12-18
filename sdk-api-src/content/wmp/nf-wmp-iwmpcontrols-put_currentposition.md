---
UID: NF:wmp.IWMPControls.put_currentPosition
title: IWMPControls::put_currentPosition
author: windows-sdk-content
description: The put_currentPosition method specifies the current position in the media item in seconds from the beginning.
old-location: wmp\iwmpcontrols_put_currentposition.htm
tech.root: WMP
ms.assetid: 7deedeed-8ce9-4fd7-9825-817204a9cb3e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPControls interface [Windows Media Player],put_currentPosition method, IWMPControls.put_currentPosition, IWMPControls::put_currentPosition, IWMPControlsput_currentPosition, put_currentPosition, put_currentPosition method [Windows Media Player], put_currentPosition method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_put_currentposition, wmp/IWMPControls::put_currentPosition
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
 - IWMPControls.put_currentPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd563179(v=VS.85).aspx">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563199(v=VS.85).aspx">IWMPControls::get_currentPosition</a>
 

 

