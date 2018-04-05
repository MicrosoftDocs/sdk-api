---
UID: NF:wmsdkidl.IWMReaderAdvanced5.SetPlayerHook
title: IWMReaderAdvanced5::SetPlayerHook method
author: windows-driver-content
description: The SetPlayerHook method assigns a player-hook callback to the reader. The reader calls the callback method before sending each sample to the graphics processor for decompression.
old-location: wmformat\iwmreaderadvanced5_setplayerhook.htm
old-project: wmformat
ms.assetid: 499c6c31-8cdf-4b99-964a-1fd51c14c5bd
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMReaderAdvanced5, IWMReaderAdvanced5 interface [windows Media Format], SetPlayerHook method, IWMReaderAdvanced5::SetPlayerHook, IWMReaderAdvanced5SetPlayerHook, SetPlayerHook method [windows Media Format], SetPlayerHook method [windows Media Format], IWMReaderAdvanced5 interface, SetPlayerHook,IWMReaderAdvanced5.SetPlayerHook, wmformat.iwmreaderadvanced5_setplayerhook, wmsdkidl/IWMReaderAdvanced5::SetPlayerHook
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK with update number 888656 installed, or later versions of the SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced5.SetPlayerHook
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced5::SetPlayerHook method


## -description



The <b>SetPlayerHook</b> method assigns a player-hook callback to the reader. The reader calls the callback method before sending each sample to the graphics processor for decompression.




## -parameters




### -param dwOutputNum [in]

The output number to which the player-hook callback applies.


### -param pHook [in]

Pointer to the implementation of the <a href="https://msdn.microsoft.com/5e58cb6a-3398-4b12-881e-76f936f6c7b3">IWMPlayerHook</a> interface that will be used in association with the specified output.


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



DirectX Video Acceleration enables supported graphics cards to decompress video samples.




## -see-also




<a href="https://msdn.microsoft.com/28d697d8-99b5-4968-a765-ba01b86914f6">IWMReaderAdvanced5 Interface</a>
 

 

