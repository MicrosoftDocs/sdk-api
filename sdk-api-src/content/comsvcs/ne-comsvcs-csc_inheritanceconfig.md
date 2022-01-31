---
UID: NE:comsvcs.tagCSC_InheritanceConfig
title: CSC_InheritanceConfig (comsvcs.h)
description: Indicates whether to create a new context based on the current context or to create a new context based solely upon the information in CServiceConfig.
helpviewer_keywords: ["CSC_Ignore","CSC_Inherit","CSC_InheritanceConfig","CSC_InheritanceConfig enumeration [COM+]","_cos_csc_inheritanceconfig","comsvcs/CSC_Ignore","comsvcs/CSC_Inherit","comsvcs/CSC_InheritanceConfig","cos.csc_inheritanceconfig"]
old-location: cos\csc_inheritanceconfig.htm
tech.root: cos
ms.assetid: 9bc8c4f3-d13e-46b6-9187-904b05f66f66
ms.date: 12/05/2018
ms.keywords: CSC_Ignore, CSC_Inherit, CSC_InheritanceConfig, CSC_InheritanceConfig enumeration [COM+], _cos_csc_inheritanceconfig, comsvcs/CSC_Ignore, comsvcs/CSC_Inherit, comsvcs/CSC_InheritanceConfig, cos.csc_inheritanceconfig
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CSC_InheritanceConfig
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSC_InheritanceConfig
 - comsvcs/tagCSC_InheritanceConfig
 - CSC_InheritanceConfig
 - comsvcs/CSC_InheritanceConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_InheritanceConfig
---

# CSC_InheritanceConfig enumeration


## -description

Indicates whether to create a new context based on the current context or to create a new context based solely upon the information in <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>.

## -enum-fields

### -field CSC_Inherit:0

The new context is created from the existing context.

### -field CSC_Ignore

The new context is created from the default context.

## -remarks

The different values of this enumeration can be used to establish the default configurations for the various services provided through <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>. The default inheritance configuration for <b>CServiceConfig</b> is CSC_Ignore. It is often useful to use CSC_Ignore when calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>, while CSC_Inherit is useful when augmenting an existing context, such as when calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.

Calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceinheritanceconfig-containingcontexttreatment">IServiceInheritanceConfig::ContainingContextTreatment</a> overwrites any previous configuration settings of the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object with the following defaults.

<h3><a id="For_CSC_InheritanceConfig_set_to_CSC_Inherit"></a><a id="for_csc_inheritanceconfig_set_to_csc_inherit"></a><a id="FOR_CSC_INHERITANCECONFIG_SET_TO_CSC_INHERIT"></a>For CSC_InheritanceConfig set to CSC_Inherit</h3>
<table>
<tr>
<th>Enumeration</th>
<th>Default</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_comtiintrinsicsconfig">CSC_COMTIIntrinsicsConfig</a>
</td>
<td>CSC_InheritCOMTIIntrinsics</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_iisintrinsicsconfig">CSC_IISIntrinsicsConfig</a>
</td>
<td>CSC_InheritIISIntrinsics</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_partitionconfig">CSC_PartitionConfig</a>
</td>
<td>CSC_InheritPartition</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_sxsconfig">CSC_SxsConfig</a>
</td>
<td>CSC_InheritSxs</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_synchronizationconfig">CSC_SynchronizationConfig</a>
</td>
<td>CSC_IfContainerIsSynchronized</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_threadpool">CSC_ThreadPool</a>
</td>
<td>CSC_ThreadPoolInherit</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_transactionconfig">CSC_TransactionConfig</a>
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
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_comtiintrinsicsconfig">CSC_COMTIIntrinsicsConfig</a>
</td>
<td>CSC_NoCOMTIIntrinsics</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_iisintrinsicsconfig">CSC_IISIntrinsicsConfig</a>
</td>
<td>CSC_NoIISIntrinsics</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_partitionconfig">CSC_PartitionConfig</a>
</td>
<td>CSC_NoPartition</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_sxsconfig">CSC_SxsConfig</a>
</td>
<td>CSC_NoSxs</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_synchronizationconfig">CSC_SynchronizationConfig</a>
</td>
<td>CSC_NoSynchronization</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_threadpool">CSC_ThreadPool</a>
</td>
<td>CSC_ThreadPoolNone</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_transactionconfig">CSC_TransactionConfig</a>
</td>
<td>CSC_NoTransaction</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceinheritanceconfig-containingcontexttreatment">IServiceInheritanceConfig::ContainingContextTreatment</a>
