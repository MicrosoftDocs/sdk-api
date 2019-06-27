---
UID: NF:wmcontainer.IMFASFStreamConfig.GetPayloadExtensionCount
title: IMFASFStreamConfig::GetPayloadExtensionCount (wmcontainer.h)
author: windows-sdk-content
description: Retrieves the number of payload extensions that are configured for the stream.
old-location: mf\imfasfstreamconfig_getpayloadextensioncount.htm
tech.root: medfound
ms.assetid: 3b1cb5a9-e39c-4f16-abc1-45ab516a4b80
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3b1cb5a9-e39c-4f16-abc1-45ab516a4b80, GetPayloadExtensionCount, GetPayloadExtensionCount method [Media Foundation], GetPayloadExtensionCount method [Media Foundation],IMFASFStreamConfig interface, IMFASFStreamConfig interface [Media Foundation],GetPayloadExtensionCount method, IMFASFStreamConfig.GetPayloadExtensionCount, IMFASFStreamConfig::GetPayloadExtensionCount, mf.imfasfstreamconfig_getpayloadextensioncount, wmcontainer/IMFASFStreamConfig::GetPayloadExtensionCount
ms.topic: method
f1_keywords: 
 - "wmcontainer/IMFASFStreamConfig.GetPayloadExtensionCount"
req.header: wmcontainer.h
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
 - IMFASFStreamConfig.GetPayloadExtensionCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFStreamConfig::GetPayloadExtensionCount


## -description



Retrieves the number of payload extensions that are configured for the stream.




## -parameters




### -param pcPayloadExtensions [out]

Receives the number of payload extensions.


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension">IMFASFStreamConfig::GetPayloadExtension</a>
 

 

