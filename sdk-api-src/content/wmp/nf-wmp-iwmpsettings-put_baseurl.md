---
UID: NF:wmp.IWMPSettings.put_baseURL
title: IWMPSettings::put_baseURL
author: windows-driver-content
description: The put_baseURL method specifies the base URL used for relative path resolution with URL script commands that are embedded in digital media files.
old-location: wmp\iwmpsettings_put_baseurl.htm
old-project: WMP
ms.assetid: ae070004-e90e-4f1e-b8b8-15deccdc48ad
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_baseURL method, IWMPSettings.put_baseURL, IWMPSettings::put_baseURL, IWMPSettingsput_baseURL, put_baseURL, put_baseURL method [Windows Media Player], put_baseURL method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_baseurl, wmp/IWMPSettings::put_baseURL
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
-	IWMPSettings.put_baseURL
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings::put_baseURL


## -description



The <b>put_baseURL</b> method specifies the base URL used for relative path resolution with URL script commands that are embedded in digital media files.




## -parameters




### -param bstrBaseURL [in]

<b>BSTR</b> containing the base URL.


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



This method specifies the base HTTP URL that is passed as the command parameter by the <b>ScriptCommand</b> event. The base URL is concatenated with the relative URL as follows:

<ol>
<li>A trailing forward slash (/) is added to the value specified in the <b>put_baseURL</b> method.</li>
<li>A leading period, backward slash, or forward slash character (., \, and /) is deleted from the relative URL.</li>
<li>The relative URL is added to the end of the base URL.</li>
<li>All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</li>
</ol>
<b>Note</b>

The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/1010961f-6d06-455a-9c14-bc06702e9e89">IWMPEvents::ScriptCommand</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/2e4a2696-624f-4c6f-8947-2fe0b457332c">IWMPSettings::get_baseURL</a>
 

 

