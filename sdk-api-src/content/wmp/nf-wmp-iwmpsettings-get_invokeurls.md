---
UID: NF:wmp.IWMPSettings.get_invokeURLs
title: IWMPSettings::get_invokeURLs method
author: windows-driver-content
description: The get_invokeURLs method retrieves a value indicating whether URL events should launch a Web browser.
old-location: wmp\iwmpsettings_get_invokeurls.htm
old-project: WMP
ms.assetid: a29ea1ba-8994-4d0f-8c53-8abba8fe997d
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPSettings, IWMPSettings interface [Windows Media Player], get_invokeURLs method, IWMPSettings::get_invokeURLs, IWMPSettingsget_invokeURLs, get_invokeURLs method [Windows Media Player], get_invokeURLs method [Windows Media Player], IWMPSettings interface, get_invokeURLs,IWMPSettings.get_invokeURLs, wmp.iwmpsettings_get_invokeurls, wmp/IWMPSettings::get_invokeURLs
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPSettings.get_invokeURLs
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::get_invokeURLs method


## -description



The <b>get_invokeURLs</b> method retrieves a value indicating whether URL events should launch a Web browser.




## -parameters




### -param pfInvokeURLs [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether URL events should launch a Web browser. The default is <b>TRUE</b>.


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



Digital media files and streams can contain URL script commands. When a URL script command is sent to the Windows Media Player control, it is passed first to the <b>ScriptCommand</b> event handler regardless of the value retrieved by <b>get_invokeURLs</b>. After <b>ScriptCommand</b> exits, Windows Media Player checks the <b>VARIANT_BOOL</b> retrieved by <b>get_invokeURLs</b> to determine whether to launch the default Web browser with the URL. You can selectively display URLs by checking them in <b>ScriptCommand</b> and setting <b>put_invokeURLs</b> as needed.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/1010961f-6d06-455a-9c14-bc06702e9e89">IWMPEvents::ScriptCommand</a>



<a href="https://msdn.microsoft.com/4c62ba8e-8fca-4cfe-9a52-6b6ac2c7c0de">IWMPSettigns::put_invokeURLs</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>
 

 

