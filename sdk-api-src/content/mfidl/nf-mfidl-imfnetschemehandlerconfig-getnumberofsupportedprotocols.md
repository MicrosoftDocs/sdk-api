---
UID: NF:mfidl.IMFNetSchemeHandlerConfig.GetNumberOfSupportedProtocols
title: IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols (mfidl.h)
author: windows-sdk-content
description: Retrieves the number of protocols supported by the network scheme plug-in.
old-location: mf\imfnetschemehandlerconfig_getnumberofsupportedprotocols.htm
tech.root: medfound
ms.assetid: a0cbb01c-c86c-4186-81ca-6055aab5d361
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNumberOfSupportedProtocols, GetNumberOfSupportedProtocols method [Media Foundation], GetNumberOfSupportedProtocols method [Media Foundation],IMFNetSchemeHandlerConfig interface, IMFNetSchemeHandlerConfig interface [Media Foundation],GetNumberOfSupportedProtocols method, IMFNetSchemeHandlerConfig.GetNumberOfSupportedProtocols, IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols, a0cbb01c-c86c-4186-81ca-6055aab5d361, mf.imfnetschemehandlerconfig_getnumberofsupportedprotocols, mfidl/IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols
ms.topic: method
f1_keywords: 
 - "mfidl/IMFNetSchemeHandlerConfig.GetNumberOfSupportedProtocols"
req.header: mfidl.h
req.include-header: 
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetSchemeHandlerConfig.GetNumberOfSupportedProtocols
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols


## -description



Retrieves the number of protocols supported by the network scheme plug-in.




## -parameters




### -param pcProtocols [out]

Receives the number of protocols.


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig">IMFNetSchemeHandlerConfig</a>
 

 

