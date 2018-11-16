---
UID: NF:wmp.IWMPCdromBurn.get_burnFormat
title: IWMPCdromBurn::get_burnFormat
author: windows-sdk-content
description: The get_burnFormat method retrieves a value that indicates the type of CD to burn.
old-location: wmp\iwmpcdromburn_get_burnformat.htm
tech.root: WMP
ms.assetid: 564a3978-555e-4cbc-90fe-b29f61349260
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_burnFormat method, IWMPCdromBurn.get_burnFormat, IWMPCdromBurn::get_burnFormat, IWMPCdromBurnget_burnFormat, get_burnFormat, get_burnFormat method [Windows Media Player], get_burnFormat method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_burnformat, wmp/IWMPCdromBurn::get_burnFormat
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
 - IWMPCdromBurn.get_burnFormat
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
- IWMPCdromBurn.get_burnFormat
: 
---

# IWMPCdromBurn::get_burnFormat


## -description



The <b>get_burnFormat</b> method retrieves a value that indicates the type of CD to burn.




## -parameters




### -param pwmpbf [out]

Pointer to a variable that receives a value from the <b>WMPBurnFormat</b> enumeration that indicates the type of CD to burn.


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



<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>



<a href="https://msdn.microsoft.com/1352e2f6-cad8-4d86-b973-b7d4d8f0c448">IWMPCdromBurn::put_burnFormat</a>



<a href="https://msdn.microsoft.com/5761dbfb-4e7d-4063-bde7-2aa9d7869d7c">WMPBurnFormat</a>
 

 

