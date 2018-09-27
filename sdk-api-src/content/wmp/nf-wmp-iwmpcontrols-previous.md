---
UID: NF:wmp.IWMPControls.previous
title: IWMPControls::previous
author: windows-sdk-content
description: The previous method sets the previous item in the playlist as the current item.
old-location: wmp\iwmpcontrols_previous.htm
tech.root: WMP
ms.assetid: e26eca59-1e2d-4a1f-b133-e337a934014b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPControls interface [Windows Media Player],previous method, IWMPControls.previous, IWMPControls::previous, IWMPControlsprevious, previous, previous method [Windows Media Player], previous method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_previous, wmp/IWMPControls::previous
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
 - IWMPControls.previous
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls::previous


## -description



The <b>previous</b> method sets the previous item in the playlist as the current item.




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



If the playlist is on the first entry when <b>previous</b> is invoked, the last entry in the playlist will become the current one.




## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/1f0bbc77-b271-4076-8089-92fe7745d9a8">IWMPControls::next</a>



<a href="https://msdn.microsoft.com/97ab009d-5ad9-4049-a212-1ef95941f951">IWMPControls::stop</a>
 

 

