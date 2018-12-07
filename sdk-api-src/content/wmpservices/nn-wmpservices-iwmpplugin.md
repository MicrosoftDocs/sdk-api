---
UID: NN:wmpservices.IWMPPlugin
title: IWMPPlugin
author: windows-sdk-content
description: The IWMPPlugin interface is implemented by the plug-in. It manages the connection to Windows Media Player.Note  The interface identifier GUID for this interface changed between the beta release and the final release. .
old-location: wmp\iwmpplugin.htm
tech.root: WMP
ms.assetid: e384aa43-72ab-44b7-b6bd-7a29335b5197
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPlugin, IWMPPlugin interface [Windows Media Player], IWMPPlugin interface [Windows Media Player],described, IWMPPluginInterfaceDSP, wmp.iwmpplugin, wmpservices/IWMPPlugin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPPlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlugin interface


## -description



The <b>IWMPPlugin</b> interface is implemented by the plug-in. It manages the connection to Windows Media Player.

<div class="alert"><b>Note</b>  The interface identifier GUID for this interface changed between the beta release and the final release.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/203b9363-1363-48be-8ba6-8b152ae9a92f">AdviseWMPServices</a>
</td>
<td align="left" width="63%">
Receives a pointer to a Windows Media Player interface that contains methods that provide stream state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8b38453-47a3-4330-88f8-8d8993089f75">GetCaps</a>
</td>
<td align="left" width="63%">
Sets a value that specifies whether the plug-in requires the input format and output format to be identical.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/883b6e19-5d1a-4ad9-882b-953772e8e11a">GetID</a>
</td>
<td align="left" width="63%">
Returns the Class ID of the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/812752d5-4d4b-4d8d-86a7-c7a9daa092e5">Init</a>
</td>
<td align="left" width="63%">
Receives a playback context identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80a8fe19-3660-49cb-8bbb-0267b3f11b63">Shutdown</a>
</td>
<td align="left" width="63%">
Executes when Windows Media Player shuts down the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/377a6853-94fb-4467-a893-508b56637a16">UnAdviseWMPServices</a>
</td>
<td align="left" width="63%">
Executes when Windows Media Player releases the pointer provided in <b>AdviseWMPServices</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4660f928-2e92-468f-9e2b-b411931dfded">DSP Plug-in Interfaces</a>
 

 

