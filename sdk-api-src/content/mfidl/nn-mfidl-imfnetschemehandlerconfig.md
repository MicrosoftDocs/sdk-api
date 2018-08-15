---
UID: NN:mfidl.IMFNetSchemeHandlerConfig
title: IMFNetSchemeHandlerConfig
author: windows-sdk-content
description: Configures a network scheme plug-in.
old-location: mf\imfnetschemehandlerconfig.htm
old-project: medfound
ms.assetid: 91bdcdbd-d621-42e3-8e0f-f8eeab489d35
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 91bdcdbd-d621-42e3-8e0f-f8eeab489d35, IMFNetSchemeHandlerConfig, IMFNetSchemeHandlerConfig interface [Media Foundation], IMFNetSchemeHandlerConfig interface [Media Foundation],described, mf.imfnetschemehandlerconfig, mfidl/IMFNetSchemeHandlerConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetSchemeHandlerConfig
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetSchemeHandlerConfig interface


## -description


Configures a network scheme plug-in.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetSchemeHandlerConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetSchemeHandlerConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetSchemeHandlerConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0cbb01c-c86c-4186-81ca-6055aab5d361">GetNumberOfSupportedProtocols</a>
</td>
<td align="left" width="63%">
Retrieves the number of protocols supported by the network scheme plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51cd90cf-a3ae-45dd-bc27-c91d44cab9f5">GetSupportedProtocolType</a>
</td>
<td align="left" width="63%">
Retrieves the protocol type for a given protocol index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2f792a4-811b-4eec-849b-bdd22774c4a8">ResetProtocolRolloverSettings</a>
</td>
<td align="left" width="63%">
Not implemented in this release.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/3c026426-c2b7-4909-9524-9cc0bd45347e">Supported Protocols</a>
 

 

