---
UID: NF:wmp.IWMPPlayerServices.setTaskPaneURL
title: IWMPPlayerServices::setTaskPaneURL method
author: windows-driver-content
description: This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK. It may be unavailable in subsequent versions.
old-location: wmp\iwmpplayerservices_settaskpaneurl.htm
old-project: WMP
ms.assetid: 4ceacaeb-09af-4cdf-84b7-04574a83ec48
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPPlayerServices, IWMPPlayerServices interface [Windows Media Player], setTaskPaneURL method, IWMPPlayerServices::setTaskPaneURL, IWMPPlayerServicessetTaskPaneURLdeprecated, setTaskPaneURL method [Windows Media Player], setTaskPaneURL method [Windows Media Player], IWMPPlayerServices interface, setTaskPaneURL,IWMPPlayerServices.setTaskPaneURL, wmp.iwmpplayerservices_settaskpaneurl, wmp/IWMPPlayerServices::setTaskPaneURL
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
-	IWMPPlayerServices.setTaskPaneURL
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayerServices::setTaskPaneURL method


## -description




          This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK. It may be unavailable in subsequent versions.
        



The <b>setTaskPaneURL</b> method displays the specified URL in the specified task pane of the full mode of Windows Media Player.


## -parameters




### -param bstrTaskPane [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MediaGuide</td>
<td>Opens Windows Media Player in the <b>MediaGuide</b> feature.</td>
</tr>
<tr>
<td>RadioTuner</td>
<td>Opens Windows Media Player in the <b>RadioTuner</b> feature.</td>
</tr>
<tr>
<td>Services</td>
<td>Opens Windows Media Player in the <b>Premium Services</b> feature.</td>
</tr>
</table>
 


### -param bstrURL [in]

<b>BSTR</b> containing the URL to display in the task pane.


### -param bstrFriendlyName [in]

<b>BSTR</b> containing the friendly name of the content at the specified URL.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>
 




## -remarks



This method is used only when remoting the Windows Media Player control. This method must be called when the control is in the docked state. Once set, the specified task pane is opened the next time the remoted control transitions to Windows Media Player.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/3d9ca91f-c672-4ecb-a6db-67d7e1ddbe7e">IWMPPlayerServices Interface</a>



<a href="https://msdn.microsoft.com/4b34ec95-d9a3-4135-b369-39955199ac00">IWMPPlayerServices::setTaskPane</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

