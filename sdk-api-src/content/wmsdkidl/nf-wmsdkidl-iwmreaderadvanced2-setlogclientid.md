---
UID: NF:wmsdkidl.IWMReaderAdvanced2.SetLogClientID
title: IWMReaderAdvanced2::SetLogClientID
author: windows-sdk-content
description: The SetLogClientID method specifies whether the reader logs the client's unique ID or an anonymous session ID.
old-location: wmformat\iwmreaderadvanced2_setlogclientid.htm
old-project: wmformat
ms.assetid: 818b7a0e-bbf4-42b2-a5a4-75078834c9f6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],SetLogClientID method, IWMReaderAdvanced2.SetLogClientID, IWMReaderAdvanced2::SetLogClientID, IWMReaderAdvanced2SetLogClientID, SetLogClientID, SetLogClientID method [windows Media Format], SetLogClientID method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_setlogclientid, wmsdkidl/IWMReaderAdvanced2::SetLogClientID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderAdvanced2.SetLogClientID
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced2::SetLogClientID


## -description



The <b>SetLogClientID</b> method specifies whether the reader logs the client's unique ID or an anonymous session ID.




## -parameters




### -param fLogClientID [in]

Specify one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>TRUE</td>
<td>Send the client's unique ID.</td>
</tr>
<tr>
<td>FALSE</td>
<td>Send an anonymous session ID.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



When the reader object streams content over the network, it sends logging data to the originating server. This logging information includes a GUID that identifies the session. By default, the reader generates an anonymous session ID. If the value of <i>fLogClientID</i> is <b>TRUE</b>, the reader sends an ID that uniquely identifies the current user. The unique ID is stored in the registry under HKEY_CURRENT_USER. If the key does not exist, the reader creates it dynamically.

Anonymous session IDs always have the following form:

<pre class="syntax" xml:space="preserve"><code>
3300AD50-2C39-46c0-AE0A-XXXXXXXXXXXX
</code></pre>
where the last six bytes are randomly generated.




## -see-also




<a href="https://msdn.microsoft.com/3e0d0fea-4370-41f8-b461-73a37de8d8bc">Client Logging</a>



<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/034ad344-2266-4662-9797-70031f58f0cd">IWMReaderAdvanced2::GetLogClientID</a>
 

 

