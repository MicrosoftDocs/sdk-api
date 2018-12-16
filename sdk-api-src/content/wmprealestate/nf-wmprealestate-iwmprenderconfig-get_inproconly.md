---
UID: NF:wmprealestate.IWMPRenderConfig.get_inProcOnly
title: IWMPRenderConfig::get_inProcOnly
author: windows-sdk-content
description: The get_inProcOnly method retrieves a value indicating whether playback is restricted to the current process.
old-location: wmp\iwmprenderconfig_get_inproconly.htm
tech.root: WMP
ms.assetid: 71284af6-dc76-4a39-81f4-ed265140aad5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPRenderConfig interface [Windows Media Player],get_inProcOnly method, IWMPRenderConfig.get_inProcOnly, IWMPRenderConfig::get_inProcOnly, IWMPRenderConfiggetInProcOnly, get_inProcOnly, get_inProcOnly method [Windows Media Player], get_inProcOnly method [Windows Media Player],IWMPRenderConfig interface, wmp.iwmprenderconfig_get_inproconly, wmprealestate/IWMPRenderConfig::get_inProcOnly
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
 - IWMPRenderConfig.get_inProcOnly
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPRenderConfig::get_inProcOnly


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563639(v=VS.85).aspx">IWMPRenderConfig Interface</a>
 

 

