---
UID: NF:wmp.IWMPCdromBurn.get_burnProgress
title: IWMPCdromBurn::get_burnProgress
author: windows-sdk-content
description: The get_burnProgress method retrieves the CD burning progress as percent complete.
old-location: wmp\iwmpcdromburn_get_burnprogress.htm
tech.root: WMP
ms.assetid: 4941e1be-1ed2-4d8e-ad16-79ddbdcd71bf
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_burnProgress method, IWMPCdromBurn.get_burnProgress, IWMPCdromBurn::get_burnProgress, IWMPCdromBurnget_burnProgress, get_burnProgress, get_burnProgress method [Windows Media Player], get_burnProgress method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_burnprogress, wmp/IWMPCdromBurn::get_burnProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromBurn.get_burnProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPCdromBurn.get_burnProgress
: 
---

# IWMPCdromBurn::get_burnProgress


## -description



The <b>get_burnProgress</b> method retrieves the CD burning progress as percent complete.




## -parameters




### -param plProgress [out]

Pointer to a <b>long</b> that receives the progress value. Progress values range from 0 to 100.


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



The progress value represents the completed percentage of the entire burning process, including any staging operations.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>
 

 

