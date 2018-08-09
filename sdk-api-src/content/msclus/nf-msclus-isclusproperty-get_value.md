---
UID: NF:msclus.ISClusProperty.get_Value
title: ISClusProperty::get_Value
author: windows-sdk-content
description: Locally stored copy of the property value of a cluster object property.
old-location: mscs\clusproperty_value.htm
old-project: mscs
ms.assetid: 415458fc-0902-421f-ac00-ee46e24dc8ee
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusProperty object [Failover Cluster],Value property, ClusProperty.Value, ISClusProperty.get_Value, ISClusProperty::get_Value, Value property [Failover Cluster], Value property [Failover Cluster],ClusProperty object, _wolf_clusproperty.value, get_Value, mscs.clusproperty_value
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusProperty.Value
 - ISClusProperty.get_Value
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperty::get_Value


## -description


<p class="CCE_Message">[The <b>Value</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Sets or retrieves the 
    locally stored copy of the <a href="https://msdn.microsoft.com/en-us/library/Aa371816(v=VS.85).aspx">property value</a> 
    of a <a href="https://msdn.microsoft.com/ba11ba7a-10f7-4f2c-99cd-d274912ad454">cluster object property</a>.

This property is read-only.


## -parameters


## -remarks



A <a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a> object operates on a local copy 
    of cluster property data. Changes made to the local copy of the data do not take effect in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> until the parent 
    <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection invokes the 
    <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a> method. Any change 
    to the local copy of the property value causes 
    <a href="https://msdn.microsoft.com/5eaeffda-e2ce-420a-b3f5-da8dfbfdde24">ClusProperties.Modified</a> to return 
    <b>VARIANT_TRUE</b>.

For detailed information about the properties associated with 
    <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a>, see 
    <a href="https://msdn.microsoft.com/ba11ba7a-10f7-4f2c-99cd-d274912ad454">Cluster Object Properties</a>.

For cluster object properties that contain multiple values, use 
    <a href="https://msdn.microsoft.com/894b4ce9-422e-481f-81a5-8cccae3140a6">ClusProperty.ValueCount</a> to find the number of 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371816(v=VS.85).aspx">property values</a>, and 
    <a href="https://msdn.microsoft.com/53cff9ea-15e4-4408-8e25-23219b8cfe76">ClusProperty.Values</a> to obtain a 
    <a href="https://msdn.microsoft.com/18ae71ee-5582-4ac9-bb0f-f1c077c0352a">ClusPropertyValues</a> collection 
    containing the property values.




## -see-also




<a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a>



<a href="https://msdn.microsoft.com/5eaeffda-e2ce-420a-b3f5-da8dfbfdde24">ClusProperties.Modified</a>



<a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a>



<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>



<a href="https://msdn.microsoft.com/894b4ce9-422e-481f-81a5-8cccae3140a6">ClusProperty.ValueCount</a>



<a href="https://msdn.microsoft.com/53cff9ea-15e4-4408-8e25-23219b8cfe76">ClusProperty.Values</a>



<a href="https://msdn.microsoft.com/18ae71ee-5582-4ac9-bb0f-f1c077c0352a">ClusPropertyValues</a>
 

 

