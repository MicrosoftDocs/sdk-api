---
UID: NF:wmprealestate.IWMPRenderConfig.put_inProcOnly
title: IWMPRenderConfig::put_inProcOnly method
author: windows-driver-content
description: The put_inProcOnly method specifies a value indicating whether playback is restricted to the current process.
old-location: wmp\iwmprenderconfig_put_inproconly.htm
old-project: WMP
ms.assetid: fd7c7cbc-f428-46e1-b239-74b78cbf5835
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPRenderConfig, IWMPRenderConfig interface [Windows Media Player], put_inProcOnly method, IWMPRenderConfig::put_inProcOnly, IWMPRenderConfigputInProcOnly, put_inProcOnly method [Windows Media Player], put_inProcOnly method [Windows Media Player], IWMPRenderConfig interface, put_inProcOnly,IWMPRenderConfig.put_inProcOnly, wmp.iwmprenderconfig_put_inproconly, wmprealestate/IWMPRenderConfig::put_inProcOnly
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmprealestate.h
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
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPRenderConfig.put_inProcOnly
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPRenderConfig::put_inProcOnly method


## -description



The <b>put_inProcOnly</b> method specifies a value indicating whether playback is restricted to the current process.




## -parameters




### -param fInProc [in]

<b>BOOL</b>, <b>TRUE</b> specifying that playback is restricted to the current process.


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



Using this method with protected content is not supported.

This method can be helpful when debugging. If your program works with the Media Foundation topology directly (for example, specifying an EVR presenter by using the <a href="https://msdn.microsoft.com/60318e68-89dd-4505-a703-3de4d5442236">IWMPVideoRenderConfig</a> interface), it might be easier to debug your code when the presenter is in the same process.

This method might also be useful if your Media Foundation components are designed to run in the main program's process.

Note that DirectShow graphs in Windows Media Player always run in the main process.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/01a4c79e-9867-47c0-9aca-b2f1596f1c2a">IWMPRenderConfig Interface</a>
 

 

