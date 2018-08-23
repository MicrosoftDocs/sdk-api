---
UID: NE:comsvcs.tagCSC_InheritanceConfig
title: tagCSC_InheritanceConfig
author: windows-sdk-content
description: Indicates whether to create a new context based on the current context or to create a new context based solely upon the information in CServiceConfig.
old-location: cos\csc_inheritanceconfig.htm
old-project: cossdk
ms.assetid: 9bc8c4f3-d13e-46b6-9187-904b05f66f66
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CSC_Ignore, CSC_Inherit, CSC_InheritanceConfig, CSC_InheritanceConfig enumeration [COM+], _cos_csc_inheritanceconfig, comsvcs/CSC_Ignore, comsvcs/CSC_Inherit, comsvcs/CSC_InheritanceConfig, cos.csc_inheritanceconfig, tagCSC_InheritanceConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CSC_InheritanceConfig
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_InheritanceConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagCSC_InheritanceConfig enumeration


## -description


Indicates whether to create a new context based on the current context or to create a new context based solely upon the information in <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>.


## -enum-fields




### -field CSC_Inherit

The new context is created from the existing context.


### -field CSC_Ignore

The new context is created from the default context.


## -remarks



The different values of this enumeration can be used to establish the default configurations for the various services provided through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>. The default inheritance configuration for <b>CServiceConfig</b> is CSC_Ignore. It is often useful to use CSC_Ignore when calling <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>, while CSC_Inherit is useful when augmenting an existing context, such as when calling <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>.

Calling <a href="https://msdn.microsoft.com/05009c50-1d39-46f7-b549-281342d07f5b">IServiceInheritanceConfig::ContainingContextTreatment</a> overwrites any previous configuration settings of the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object with the following defaults.

<h3><a id="For_CSC_InheritanceConfig_set_to_CSC_Inherit"></a><a id="for_csc_inheritanceconfig_set_to_csc_inherit"></a><a id="FOR_CSC_INHERITANCECONFIG_SET_TO_CSC_INHERIT"></a>For CSC_InheritanceConfig set to CSC_Inherit</h3>
<table>
<tr>
<th>Enumeration</th>
<th>Default</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0d700648-b5fe-46f6-9d27-e2601fe88d71">CSC_COMTIIntrinsicsConfig</a>
</td>
<td>CSC_InheritCOMTIIntrinsics</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/69a3989b-724c-4e32-8a6a-4892610b0118">CSC_IISIntrinsicsConfig</a>
</td>
<td>CSC_InheritIISIntrinsics</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/584c4744-193d-43d4-a305-8f4ea9802d58">CSC_PartitionConfig</a>
</td>
<td>CSC_InheritPartition</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8c114e9e-b201-4317-8a45-d5b0964c6ff8">CSC_SxsConfig</a>
</td>
<td>CSC_InheritSxs</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/dc0c4310-e2d8-462c-af55-f1513934b8ef">CSC_SynchronizationConfig</a>
</td>
<td>CSC_IfContainerIsSynchronized</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5acf5c6b-b015-448b-ad4c-e4361a97c31e">CSC_ThreadPool</a>
</td>
<td>CSC_ThreadPoolInherit</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3524d7b3-4bcd-4e92-afc2-ddac98a23b7c">CSC_TransactionConfig</a>
</td>
<td>CSC_IfContainerIsTransactional</td>
</tr>
</table>
 

<h3><a id="For_CSC_InheritanceConfig_set_to_CSC_Ignore"></a><a id="for_csc_inheritanceconfig_set_to_csc_ignore"></a><a id="FOR_CSC_INHERITANCECONFIG_SET_TO_CSC_IGNORE"></a>For CSC_InheritanceConfig set to CSC_Ignore</h3>
<table>
<tr>
<th>Enumeration</th>
<th>Default</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0d700648-b5fe-46f6-9d27-e2601fe88d71">CSC_COMTIIntrinsicsConfig</a>
</td>
<td>CSC_NoCOMTIIntrinsics</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/69a3989b-724c-4e32-8a6a-4892610b0118">CSC_IISIntrinsicsConfig</a>
</td>
<td>CSC_NoIISIntrinsics</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/584c4744-193d-43d4-a305-8f4ea9802d58">CSC_PartitionConfig</a>
</td>
<td>CSC_NoPartition</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8c114e9e-b201-4317-8a45-d5b0964c6ff8">CSC_SxsConfig</a>
</td>
<td>CSC_NoSxs</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/dc0c4310-e2d8-462c-af55-f1513934b8ef">CSC_SynchronizationConfig</a>
</td>
<td>CSC_NoSynchronization</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5acf5c6b-b015-448b-ad4c-e4361a97c31e">CSC_ThreadPool</a>
</td>
<td>CSC_ThreadPoolNone</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3524d7b3-4bcd-4e92-afc2-ddac98a23b7c">CSC_TransactionConfig</a>
</td>
<td>CSC_NoTransaction</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/05009c50-1d39-46f7-b549-281342d07f5b">IServiceInheritanceConfig::ContainingContextTreatment</a>
 

 

