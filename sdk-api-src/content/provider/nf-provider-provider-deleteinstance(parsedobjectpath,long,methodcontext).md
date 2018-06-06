---
UID: NF:provider.Provider.DeleteInstance(ParsedObjectPath,long,MethodContext)
title: Provider::DeleteInstance(ParsedObjectPath,long,MethodContext)
author: windows-sdk-content
description: The DeleteInstance method is called by WMI to delete an instance.
old-location: wmi\provider_deleteinstance.htm
old-project: WmiSdk
ms.assetid: 469d2481-95ea-4d17-b0ef-095ced9c8319
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DeleteInstance, DeleteInstance method [Windows Management Instrumentation], DeleteInstance method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],DeleteInstance method, Provider.DeleteInstance, Provider.DeleteInstance(ParsedObjectPath,long,MethodContext), Provider::DeleteInstance, Provider::DeleteInstance(ParsedObjectPath,long,MethodContext), _hmm_provider_deleteinstance, provider/Provider::DeleteInstance, wmi.provider_deleteinstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: provider.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.DeleteInstance
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# Provider::DeleteInstance(ParsedObjectPath,long,MethodContext)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class is part of the WMI 
    Provider Framework which is now considered in final state, and no further development, enhancements, or updates 
    will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>DeleteInstance</b> method is called by WMI to delete an instance.


## -parameters




### -param pParsedObjectPath




### -param lFlags

Bitmask of flags with information about the delete operation. This is the value specified by the client in the <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a> function.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>

### -param pContext






#### - Instance [ref]

Instance to be deleted.


## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling function. The <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a> function lists the most common return values, although you can choose to return any COM return code.




## -remarks



WMI invokes <b>DeleteInstance</b> when a client calls <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a> against a class. Therefore, you must implement <b>DeleteInstance</b> if your framework provider supports deleting instances. The following list describes a common implementation of <b>DeleteInstance</b>:

<ol>
<li>Determine which instance the client requested by reading the key properties with one of the <b>Get</b> methods for <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>, such as <a href="https://msdn.microsoft.com/d9295ba1-19da-41a2-86d1-ec80e18e895b">CInstance::GetCHString</a>.</li>
<li>Delete the instance.</li>
</ol>
For more information about deleting instances, see <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a>.



