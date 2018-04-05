---
UID: NF:wmp.IWMPCdromBurn.put_burnFormat
title: IWMPCdromBurn::put_burnFormat method
author: windows-driver-content
description: The put_burnFormat method specifies the type of CD to burn.
old-location: wmp\iwmpcdromburn_put_burnformat.htm
old-project: WMP
ms.assetid: 1352e2f6-cad8-4d86-b973-b7d4d8f0c448
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPCdromBurn, IWMPCdromBurn interface [Windows Media Player], put_burnFormat method, IWMPCdromBurn::put_burnFormat, IWMPCdromBurnput_burnFormat, put_burnFormat method [Windows Media Player], put_burnFormat method [Windows Media Player], IWMPCdromBurn interface, put_burnFormat,IWMPCdromBurn.put_burnFormat, wmp.iwmpcdromburn_put_burnformat, wmp/IWMPCdromBurn::put_burnFormat
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPCdromBurn.put_burnFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromBurn::put_burnFormat method


## -description



The <b>put_burnFormat</b> method specifies the type of CD to burn.




## -parameters




### -param wmpbf [in]

A value from the <b>WMPBurnFormat</b> enumeration that specifies the type of CD to burn.


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



<a href="https://msdn.microsoft.com/564a3978-555e-4cbc-90fe-b29f61349260">IWMPCdromBurn::get_burnFormat</a>



<a href="https://msdn.microsoft.com/5761dbfb-4e7d-4063-bde7-2aa9d7869d7c">WMPBurnFormat</a>
 

 

