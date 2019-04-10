---
UID: NF:wmcontainer.IMFASFMultiplexer.SetFlags
title: IMFASFMultiplexer::SetFlags (wmcontainer.h)
author: windows-sdk-content
description: Sets multiplexer options.
old-location: mf\imfasfmultiplexer_setflags.htm
tech.root: medfound
ms.assetid: dac4f9b0-e83a-4e99-9a4a-ec1154c929a7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFASFMultiplexer interface [Media Foundation],SetFlags method, IMFASFMultiplexer.SetFlags, IMFASFMultiplexer::SetFlags, SetFlags, SetFlags method [Media Foundation], SetFlags method [Media Foundation],IMFASFMultiplexer interface, dac4f9b0-e83a-4e99-9a4a-ec1154c929a7, mf.imfasfmultiplexer_setflags, wmcontainer/IMFASFMultiplexer::SetFlags
ms.topic: method
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
 - IMFASFMultiplexer.SetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMultiplexer::SetFlags


## -description



Sets multiplexer options.




## -parameters




### -param dwFlags [in]

Bitwise <b>OR</b> of zero or more members of the <a href="https://msdn.microsoft.com/6989ac24-f25f-4bc8-a4b9-3e41434a0d44">MFASF_MULTIPLEXERFLAGS</a> enumeration. These flags specify which multiplexer options to use. For more information, see "Multiplexer Initialization and Leaky Bucket Settings" in <a href="https://msdn.microsoft.com/a5adc40c-abb4-4012-b6f2-eb871eaed7b9">Creating the Multiplexer Object</a>.


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




<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>
 

 

