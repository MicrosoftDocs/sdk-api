---
UID: NN:msrdc.IRdcLibrary
title: IRdcLibrary (msrdc.h)
author: windows-sdk-content
description: Is the primary interface for using RDC.
old-location: rdc\irdclibrary.htm
tech.root: rdc
ms.assetid: 941fa35c-20fa-4843-89be-26112ff7eec5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRdcLibrary, IRdcLibrary interface [Remote Differential Compression], IRdcLibrary interface [Remote Differential Compression],described, fs.irdclibrary, msrdc/IRdcLibrary, rdc.irdclibrary
ms.topic: interface
f1_keywords: 
 - "msrdc/IRdcLibrary"
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
 - IRdcLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRdcLibrary interface


## -description


The <b>IRdcLibrary</b> interface is the primary interface 
    for using RDC.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcLibrary</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-computedefaultrecursiondepth">ComputeDefaultRecursionDepth</a>
</td>
<td align="left" width="63%">
Computes the maximum level of recursion for the specified file size.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-createcomparator">CreateComparator</a>
</td>
<td align="left" width="63%">
Creates a signature comparator. The caller must create a separate signature comparator for each 
    level of recursion.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-creategenerator">CreateGenerator</a>
</td>
<td align="left" width="63%">
Creates a signature generator that will generate the specified levels of 
     signatures.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-creategeneratorparameters">CreateGeneratorParameters</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a> 
     interface pointer initialized with the  parameters necessary for a signature generator.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-createsignaturereader">CreateSignatureReader</a>
</td>
<td align="left" width="63%">
Creates a signature reader to allow an application to decode the contents of a signature 
     file.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-getrdcversion">GetRDCVersion</a>
</td>
<td align="left" width="63%">
Returns the version of the installed RDC runtime and the oldest version of the RDC interfaces 
     supported by the installed runtime.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-opengeneratorparameters">OpenGeneratorParameters</a>
</td>
<td align="left" width="63%">
Opens an existing serialized parameter block and returns an 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcgeneratorparameters">IRdcGeneratorParameters</a> interface pointer 
     initialized with the data.</p> (Inherited from <b>IRdcLibrary</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rdc/remote-differential-compression-interfaces">Remote Differential Compression Interfaces</a>
 

 

