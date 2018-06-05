---
UID: NF:wmcontainer.IMFASFMultiplexer.GetFlags
title: IMFASFMultiplexer::GetFlags
author: windows-sdk-content
description: Retrieves flags indicating the configured multiplexer options.
old-location: mf\imfasfmultiplexer_getflags.htm
old-project: medfound
ms.assetid: b0aeefb5-6996-4abb-b869-855aaa7fcde2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],GetFlags method, IMFASFMultiplexer.GetFlags, IMFASFMultiplexer::GetFlags, b0aeefb5-6996-4abb-b869-855aaa7fcde2, mf.imfasfmultiplexer_getflags, wmcontainer/IMFASFMultiplexer::GetFlags
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFMultiplexer.GetFlags
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFMultiplexer::GetFlags


## -description



Retrieves flags indicating the configured multiplexer options.




## -parameters




### -param pdwFlags [out]

Receives a bitwise <b>OR</b> of zero or more values from the <a href="https://msdn.microsoft.com/6989ac24-f25f-4bc8-a4b9-3e41434a0d44">MFASF_MULTIPLEXERFLAGS</a> enumeration. To set these flags, call <a href="https://msdn.microsoft.com/dac4f9b0-e83a-4e99-9a4a-ec1154c929a7">IMFASFMultiplexer::SetFlags</a>.


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




<a href="https://msdn.microsoft.com/a5adc40c-abb4-4012-b6f2-eb871eaed7b9">Creating the Multiplexer Object</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>
 

 

