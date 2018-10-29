---
UID: NF:wmcontainer.IMFASFMultiplexer.Initialize
title: IMFASFMultiplexer::Initialize
author: windows-sdk-content
description: Initializes the multiplexer with the data from an ASF ContentInfo object.
old-location: mf\imfasfmultiplexer_initialize.htm
tech.root: medfound
ms.assetid: 61c37bd5-3f6f-434b-ae5b-c25c5213d49f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 61c37bd5-3f6f-434b-ae5b-c25c5213d49f, IMFASFMultiplexer interface [Media Foundation],Initialize method, IMFASFMultiplexer.Initialize, IMFASFMultiplexer::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFASFMultiplexer interface, mf.imfasfmultiplexer_initialize, wmcontainer/IMFASFMultiplexer::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFASFMultiplexer.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMultiplexer::Initialize


## -description



Initializes the multiplexer with the data from an ASF ContentInfo object.




## -parameters




### -param pIContentInfo [in]

Pointer to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface of the <b>MFASFContentInfo</b> object that contains the header information of the new ASF file. The multiplexer will generate data packets for this file.


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



This call must be made once at the beginning of encoding, with <i>pIContentInfo</i> pointing to the ASF ContentInfo object that describes the content to be encoded. This enables the ASF multiplexer to see, among other things, which streams will be present in the encoding session. This call typically does not affect the data in the ASF ContentInfo object.




## -see-also




<a href="https://msdn.microsoft.com/a5adc40c-abb4-4012-b6f2-eb871eaed7b9">Creating the Multiplexer Object</a>



<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>
 

 

