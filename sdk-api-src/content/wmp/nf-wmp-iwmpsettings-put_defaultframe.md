---
UID: NF:wmp.IWMPSettings.put_defaultFrame
title: IWMPSettings::put_defaultFrame
author: windows-sdk-content
description: The put_defaultFrame method specifies the name of the frame used to display a URL that is received in a ScriptCommand event.
old-location: wmp\iwmpsettings_put_defaultframe.htm
old-project: WMP
ms.assetid: 9b035e4e-84c5-46ea-aa8a-2e66810284b2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_defaultFrame method, IWMPSettings.put_defaultFrame, IWMPSettings::put_defaultFrame, IWMPSettingsput_defaultFrame, put_defaultFrame, put_defaultFrame method [Windows Media Player], put_defaultFrame method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_defaultframe, wmp/IWMPSettings::put_defaultFrame
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.put_defaultFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::put_defaultFrame


## -description



The <b>put_defaultFrame</b> method specifies the name of the frame used to display a URL that is received in a <b>ScriptCommand</b> event.




## -parameters




### -param bstrDefaultFrame [in]

<b>BSTR</b> containing the value of the name attribute of the target FRAME element.


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



If a target frame is specified in the <b>ScriptCommand</b> event itself, this method is ignored.

This method is ignored when using the Netscape Navigator Java applet. In Navigator, each URL script command received displays the URL in a new Web browser window, regardless of the value specified in <b>put_defaultFrame</b>.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/1010961f-6d06-455a-9c14-bc06702e9e89">IWMPEvents::ScriptCommand</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/815289bb-4ca5-45da-a27e-7484ba403316">IWMPSettings::get_defaultFrame</a>
 

 

