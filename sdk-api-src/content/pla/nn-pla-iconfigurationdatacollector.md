---
UID: NN:pla.IConfigurationDataCollector
title: IConfigurationDataCollector
author: windows-sdk-content
description: Collects computer settings at the time of collection.
old-location: pla\iconfigurationdatacollector.htm
old-project: PLA
ms.assetid: 7266c02d-0f56-4754-8a67-68394a5f0158
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IConfigurationDataCollector, IConfigurationDataCollector interface [PLA], IConfigurationDataCollector interface [PLA],described, base.iconfigurationdatacollector, pla.iconfigurationdatacollector, pla/IConfigurationDataCollector
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IConfigurationDataCollector
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IConfigurationDataCollector interface


## -description


Collects computer settings at the time of collection.  You can use the configuration information to verify the system state or track changes.  PLA saves the configuration information to the file specified in the <a href="https://msdn.microsoft.com/9208baf8-0bc7-45c4-a912-7b59f4c1ca6a">IDataCollector::FileName</a> property. The contents of the file is XML that is consistent with the TraceRpt.exe schema.

To create this data collector, call the <a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">IDataCollectorCollection::CreateDataCollector</a> or <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.


## -remarks



The following example shows the XML that you can use to initialize this object if you call <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">CreateDataCollectorFromXml</a> to create it. The <a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">IDataCollector::Xml</a> property also returns this XML.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;ConfigurationDataCollector&gt;
    &lt;FileMaxCount/&gt;  
    &lt;FileMaxRecursiveDepth/&gt;  
    &lt;FileMaxTotalSize/&gt;  
    &lt;File/&gt;  &lt;!-- Specify this element for each file --&gt;
    &lt;ManagementQuery/&gt;  &lt;!-- Specify this element for each WMI query --&gt;
    &lt;QueryNetworkAdapters/&gt;
    &lt;RegistryKey/&gt;  &lt;!-- Specify this element for each registry key --&gt;
    &lt;RegistryMaxRecursiveDepth/&gt;
    &lt;SystemStateFile/&gt;  
&lt;/ConfigurationDataCollector&gt;</pre>
</td>
</tr>
</table></span></div>
Note that the example does not show the property elements inherited from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>. 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>
 

 

