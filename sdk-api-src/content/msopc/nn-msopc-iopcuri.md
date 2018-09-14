---
UID: NN:msopc.IOpcUri
title: IOpcUri
author: windows-sdk-content
description: Represents the URI of the package root or of a part that is relative to the package root.
old-location: opc\iopcuri.htm
tech.root: OPC
ms.assetid: 35ce7946-f7e7-4ac3-852f-e3fcca23d6d4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOpcUri, IOpcUri interface [Open Packaging Conventions], IOpcUri interface [Open Packaging Conventions],described, msopc/IOpcUri, opc.iopcuri
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcUri
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcUri interface


## -description


Represents the  URI of the package root or of a part that is relative to  the package root.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcUri</b> interface inherits from <a href="http://go.microsoft.com/fwlink/p/?linkid=116163">IUri</a>. <b>IOpcUri</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcUri</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bb4c351-12ef-4e26-bcb1-59f81a413588">CombinePartUri</a>
</td>
<td align="left" width="63%">
Forms the part name of the part that is referenced by the specified relative URI.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b953b4c-6e8d-4097-a6bf-618b49cdd603">GetRelationshipsPartUri</a>
</td>
<td align="left" width="63%">
Gets the part name of the Relationships part that stores relationships that have the source URI represented by the  current OPC URI object.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce98b0a6-f4b3-4f49-897a-f144af7dfc49">GetRelativeUri</a>
</td>
<td align="left" width="63%">
Forms a relative URI for a specified part, relative to the URI represented by the current OPC URI object.
            

</td>
</tr>
</table> 


## -remarks



<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this interface is the same on all supported Windows versions. For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=116163">IUri</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>
 

 

