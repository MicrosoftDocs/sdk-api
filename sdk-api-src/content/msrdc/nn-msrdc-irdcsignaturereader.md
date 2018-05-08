---
UID: NN:msrdc.IRdcSignatureReader
title: IRdcSignatureReader
author: windows-driver-content
description: Reads the signatures and the parameters used to generate the signatures.
old-location: rdc\irdcsignaturereader.htm
old-project: Rdc
ms.assetid: dec6eb10-1243-4888-9ccc-ab1f4cfb11e7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IRdcSignatureReader, IRdcSignatureReader interface [Remote Differential Compression], IRdcSignatureReader interface [Remote Differential Compression],described, fs.irdcsignaturereader, msrdc/IRdcSignatureReader, rdc.irdcsignaturereader
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IRdcSignatureReader
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRdcSignatureReader interface


## -description


The <b>IRdcSignatureReader</b> interface reads the signatures and the parameters used to generate the signatures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcSignatureReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRdcSignatureReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcSignatureReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0f4d31d-338f-49fc-9f1a-e8e31ffa1bc7">ReadHeader</a>
</td>
<td align="left" width="63%">
Reads the signature header and returns a copy of the parameters
   used to generate the signatures.</p> (Inherited from <b>IRdcSignatureReader</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/566a5442-b186-4aac-94fa-5784736a30c3">ReadSignatures</a>
</td>
<td align="left" width="63%">
Reads a block of signatures from the current position.</p> (Inherited from <b>IRdcSignatureReader</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/a3131654-e849-4a88-acec-c49a61653bad">Remote Differential Compression Interfaces</a>
 

 

