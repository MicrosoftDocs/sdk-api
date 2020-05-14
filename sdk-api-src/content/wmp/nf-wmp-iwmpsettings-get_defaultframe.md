---
UID: NF:wmp.IWMPSettings.get_defaultFrame
title: IWMPSettings::get_defaultFrame (wmp.h)
description: The get_defaultFrame method retrieves the name of the frame used to display a URL that is received in a ScriptCommand event.helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_defaultFrame method","IWMPSettings.get_defaultFrame","IWMPSettings::get_defaultFrame","IWMPSettingsget_defaultFrame","get_defaultFrame","get_defaultFrame method [Windows Media Player]","get_defaultFrame method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_defaultframe","wmp/IWMPSettings::get_defaultFrame"]
old-location: wmp\iwmpsettings_get_defaultframe.htm
tech.root: WMP
ms.assetid: 815289bb-4ca5-45da-a27e-7484ba403316
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],get_defaultFrame method, IWMPSettings.get_defaultFrame, IWMPSettings::get_defaultFrame, IWMPSettingsget_defaultFrame, get_defaultFrame, get_defaultFrame method [Windows Media Player], get_defaultFrame method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_defaultframe, wmp/IWMPSettings::get_defaultFrame
f1_keywords:
- wmp/IWMPSettings.get_defaultFrame
dev_langs:
- c++
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
- IWMPSettings.get_defaultFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSettings::get_defaultFrame


## -description



The <b>get_defaultFrame</b> method retrieves the name of the frame used to display a URL that is received in a <b>ScriptCommand</b> event.




## -parameters




### -param pbstrDefaultFrame [out]

Pointer to a <b>BSTR</b> containing the value of the name attribute of the target FRAME element.


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

This method is ignored when using the Netscape Navigator Java applet. In Navigator, each URL script command received will display the URL in a new browser window, regardless of the value retrieved by <b>get_defaultFrame</b>.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents-scriptcommand">IWMPEvents::ScriptCommand</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_defaultframe">IWMPSettings::put_defaultFrame</a>
 

 

