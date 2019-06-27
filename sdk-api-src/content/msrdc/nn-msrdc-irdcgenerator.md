---
UID: NN:msrdc.IRdcGenerator
title: IRdcGenerator (msrdc.h)
author: windows-sdk-content
description: Used to process the input data and read the parameters used by the generator.
old-location: rdc\irdcgenerator.htm
tech.root: rdc
ms.assetid: 0288318a-0974-4870-b423-87c52090eb33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRdcGenerator, IRdcGenerator interface [Remote Differential Compression], IRdcGenerator interface [Remote Differential Compression],described, fs.irdcgenerator, msrdc/IRdcGenerator, rdc.irdcgenerator
ms.topic: interface
f1_keywords: 
 - "msrdc/IRdcGenerator"
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
 - IRdcGenerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRdcGenerator interface


## -description


The <b>IRdcGenerator</b> interface is used to 
    process the input data and read the parameters used by the generator.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcGenerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcGenerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcGenerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgenerator-getgeneratorparameters">GetGeneratorParameters</a>
</td>
<td align="left" width="63%">
Returns a copy of the parameters used to create the generator.</p> (Inherited from <b>IRdcGenerator</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgenerator-process">Process</a>
</td>
<td align="left" width="63%">
Processes the input 
    data and produces 0 or more output bytes.</p> (Inherited from <b>IRdcGenerator</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rdc/remote-differential-compression-interfaces">Remote Differential Compression Interfaces</a>
 

 

