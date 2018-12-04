---
UID: NF:wmp.IWMPCore.launchURL
title: IWMPCore::launchURL
author: windows-sdk-content
description: The launchURL method sends a URL to the user's default browser.
old-location: wmp\iwmpcore_launchurl.htm
tech.root: WMP
ms.assetid: 439bb4a7-801a-4bef-b791-b8a9cb24ab34
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMPCore interface [Windows Media Player],launchURL method, IWMPCore.launchURL, IWMPCore::launchURL, IWMPCorelaunchURL, launchURL, launchURL method [Windows Media Player], launchURL method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_launchurl, wmp/IWMPCore::launchURL
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
 - IWMPCore.launchURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::launchURL


## -description



The <b>launchURL</b> method sends a URL to the user's default browser.




## -parameters




### -param bstrURL [in]

<b>BSTR</b> containing the URL.


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



This method only opens webpages using the HTTP or HTTPS protocols.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>
 

 

