---
UID: NN:msrdc.IRdcGeneratorParameters
title: IRdcGeneratorParameters
author: windows-sdk-content
description: Is the generic interface for all types of generator parameters. All generator parameter objects must support this interface.
old-location: rdc\irdcgeneratorparameters.htm
tech.root: Rdc
ms.assetid: 1b2db5c5-79eb-490a-ae03-36b0e926725d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRdcGeneratorParameters, IRdcGeneratorParameters interface [Remote Differential Compression], IRdcGeneratorParameters interface [Remote Differential Compression],described, fs.irdcgeneratorparameters, msrdc/IRdcGeneratorParameters, rdc.irdcgeneratorparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcGeneratorParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRdcGeneratorParameters interface


## -description


The <b>IRdcGeneratorParameters</b> interface 
    is the generic interface for all types of generator parameters. All generator parameter objects must 
    support this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcGeneratorParameters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRdcGeneratorParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcGeneratorParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9fd60d5-a542-4a00-becd-85c7dafbe105">GetGeneratorParametersType</a>
</td>
<td align="left" width="63%">
Returns the specific type of the parameters.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58050740-0508-4797-b1b5-7a1e2a6dc00b">GetParametersVersion</a>
</td>
<td align="left" width="63%">
Returns information about the version of RDC used to serialize the parameters.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebd41d6c-c321-4017-bcc1-a2cdf5202730">GetSerializeSize</a>
</td>
<td align="left" width="63%">
Returns the size, in bytes, of the serialized parameter data.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba0d09b0-417f-494a-a5e8-dccd08e5280a">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the parameter data into a block of memory.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/a3131654-e849-4a88-acec-c49a61653bad">Remote Differential Compression Interfaces</a>
 

 

