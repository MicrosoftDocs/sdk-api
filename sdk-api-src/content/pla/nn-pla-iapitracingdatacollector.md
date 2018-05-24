---
UID: NN:pla.IApiTracingDataCollector
title: IApiTracingDataCollector
author: windows-driver-content
description: Logs Win32 calls to Kernel32.dll, Advapi32.dll, Gdi32.dll, and User32.dll.
old-location: pla\iapitracingdatacollector.htm
old-project: PLA
ms.assetid: 8d600d35-bd2b-44fc-9da4-3c6e50e90b65
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IApiTracingDataCollector, IApiTracingDataCollector interface [PLA], IApiTracingDataCollector interface [PLA],described, base.iapitracingdatacollector, pla.iapitracingdatacollector, pla/IApiTracingDataCollector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: pla.h
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IApiTracingDataCollector
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IApiTracingDataCollector interface


## -description


Logs Win32 calls to Kernel32.dll, Advapi32.dll, Gdi32.dll, and User32.dll. Note that for security reasons, not all function calls are logged.

To create this data collector, call the <a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">IDataCollectorCollection::CreateDataCollector</a> or <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.


## -remarks



The following example shows the XML that you can use to initialize this object if you call <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">CreateDataCollectorFromXml</a> to create it. The <a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">IDataCollector::Xml</a> property also returns this XML.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;ApiTracingDataCollector&gt;
    &lt;ExcludeApis/&gt;
    &lt;ExePath/&gt; 
    &lt;IncludeApis/&gt;
    &lt;IncludeModules/&gt;
    &lt;LogApiNamesOnly/&gt;
    &lt;LogApisRecursively/&gt;
    &lt;LogFilePath/&gt;
&lt;/ApiTracingDataCollector&gt;</pre>
</td>
</tr>
</table></span></div>
Note that the example does not show the property elements inherited from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>. 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>
 

 

