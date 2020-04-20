---
UID: NF:wmprealestate.IWMPRenderConfig.put_inProcOnly
title: IWMPRenderConfig::put_inProcOnly (wmprealestate.h)
description: The put_inProcOnly method specifies a value indicating whether playback is restricted to the current process.helpviewer_keywords: ["IWMPRenderConfig interface [Windows Media Player]","put_inProcOnly method","IWMPRenderConfig.put_inProcOnly","IWMPRenderConfig::put_inProcOnly","IWMPRenderConfigputInProcOnly","put_inProcOnly","put_inProcOnly method [Windows Media Player]","put_inProcOnly method [Windows Media Player]","IWMPRenderConfig interface","wmp.iwmprenderconfig_put_inproconly","wmprealestate/IWMPRenderConfig::put_inProcOnly"]
old-location: wmp\iwmprenderconfig_put_inproconly.htm
tech.root: WMP
ms.assetid: fd7c7cbc-f428-46e1-b239-74b78cbf5835
ms.date: 12/05/2018
ms.keywords: IWMPRenderConfig interface [Windows Media Player],put_inProcOnly method, IWMPRenderConfig.put_inProcOnly, IWMPRenderConfig::put_inProcOnly, IWMPRenderConfigputInProcOnly, put_inProcOnly, put_inProcOnly method [Windows Media Player], put_inProcOnly method [Windows Media Player],IWMPRenderConfig interface, wmp.iwmprenderconfig_put_inproconly, wmprealestate/IWMPRenderConfig::put_inProcOnly
f1_keywords:
- wmprealestate/IWMPRenderConfig.put_inProcOnly
dev_langs:
- c++
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
- IWMPRenderConfig.put_inProcOnly
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPRenderConfig::put_inProcOnly


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

This method can be helpful when debugging. If your program works with the Media Foundation topology directly (for example, specifying an EVR presenter by using the <a href="https://docs.microsoft.com/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig">IWMPVideoRenderConfig</a> interface), it might be easier to debug your code when the presenter is in the same process.

This method might also be useful if your Media Foundation components are designed to run in the main program's process.

Note that DirectShow graphs in Windows Media Player always run in the main process.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig">IWMPRenderConfig Interface</a>
 

 

