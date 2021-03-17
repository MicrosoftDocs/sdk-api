---
UID: NN:pla.IConfigurationDataCollector
title: IConfigurationDataCollector (pla.h)
description: Collects computer settings at the time of collection.
helpviewer_keywords: ["IConfigurationDataCollector","IConfigurationDataCollector interface [PLA]","IConfigurationDataCollector interface [PLA]","described","base.iconfigurationdatacollector","pla.iconfigurationdatacollector","pla/IConfigurationDataCollector"]
old-location: pla\iconfigurationdatacollector.htm
tech.root: PLA
ms.assetid: 7266c02d-0f56-4754-8a67-68394a5f0158
ms.date: 12/05/2018
ms.keywords: IConfigurationDataCollector, IConfigurationDataCollector interface [PLA], IConfigurationDataCollector interface [PLA],described, base.iconfigurationdatacollector, pla.iconfigurationdatacollector, pla/IConfigurationDataCollector
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
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigurationDataCollector
 - pla/IConfigurationDataCollector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IConfigurationDataCollector
---

# IConfigurationDataCollector interface


## -description

Collects computer settings at the time of collection.  You can use the configuration information to verify the system state or track changes.  PLA saves the configuration information to the file specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filename">IDataCollector::FileName</a> property. The contents of the file is XML that is consistent with the TraceRpt.exe schema.

To create this data collector, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollector">IDataCollectorCollection::CreateDataCollector</a> or <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.

## -remarks

The following example shows the XML that you can use to initialize this object if you call <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">CreateDataCollectorFromXml</a> to create it. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">IDataCollector::Xml</a> property also returns this XML.


```xml
<ConfigurationDataCollector>
    <FileMaxCount/>  
    <FileMaxRecursiveDepth/>  
    <FileMaxTotalSize/>  
    <File/>  <!-- Specify this element for each file -->
    <ManagementQuery/>  <!-- Specify this element for each WMI query -->
    <QueryNetworkAdapters/>
    <RegistryKey/>  <!-- Specify this element for each registry key -->
    <RegistryMaxRecursiveDepth/>
    <SystemStateFile/>  
</ConfigurationDataCollector>
```


Note that the example does not show the property elements inherited from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>