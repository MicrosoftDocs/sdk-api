---
UID: NF:wmprealestate.IWMPRenderConfig.get_inProcOnly
title: IWMPRenderConfig::get_inProcOnly method
author: windows-driver-content
description: The get_inProcOnly method retrieves a value indicating whether playback is restricted to the current process.
old-location: wmp\iwmprenderconfig_get_inproconly.htm
old-project: WMP
ms.assetid: 71284af6-dc76-4a39-81f4-ed265140aad5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPRenderConfig, IWMPRenderConfig interface [Windows Media Player], get_inProcOnly method, IWMPRenderConfig::get_inProcOnly, IWMPRenderConfiggetInProcOnly, get_inProcOnly method [Windows Media Player], get_inProcOnly method [Windows Media Player], IWMPRenderConfig interface, get_inProcOnly,IWMPRenderConfig.get_inProcOnly, wmp.iwmprenderconfig_get_inproconly, wmprealestate/IWMPRenderConfig::get_inProcOnly
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
-	IWMPRenderConfig.get_inProcOnly
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPRenderConfig::get_inProcOnly method


## -description



The <b>get_inProcOnly</b> method retrieves a value indicating whether playback is restricted to the current process.




## -parameters




### -param pfInProc [in]

Pointer to a <b>BOOL</b> that receives the result. <b>TRUE</b> specifies that playback is restricted to the current process.


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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/01a4c79e-9867-47c0-9aca-b2f1596f1c2a">IWMPRenderConfig Interface</a>
 

 

