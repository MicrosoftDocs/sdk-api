---
UID: NF:provider.Provider.PutInstance(IWbemClassObject,long,MethodContext)
title: Provider::PutInstance(IWbemClassObject,long,MethodContext)
author: windows-driver-content
description: The PutInstance method updates an instance.
old-location: wmi\provider_putinstance.htm
old-project: WmiSdk
ms.assetid: c9921a00-b966-47d0-a2f3-982812ab249c
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: Provider interface [Windows Management Instrumentation],PutInstance method, Provider.PutInstance, Provider.PutInstance(IWbemClassObject,long,MethodContext), Provider::PutInstance, Provider::PutInstance(IWbemClassObject,long,MethodContext), PutInstance, PutInstance method [Windows Management Instrumentation], PutInstance method [Windows Management Instrumentation],Provider interface, _hmm_provider_putinstance, provider/Provider::PutInstance, wmi.provider_putinstance
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	Provider.PutInstance
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# Provider::PutInstance(IWbemClassObject,long,MethodContext)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class is part of the WMI 
    Provider Framework which is now considered in final state, and no further development, enhancements, or updates 
    will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>PutInstance</b> method updates an instance.


## -parameters




### -param pInst




### -param lFlags

Bitmask of flags with information about the update operation. This is the value specified by the client in the <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> method.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>
Valid <i>lFlags</i> values are:

<ul>
<li><b>WBEM_FLAG_CREATE_ONLY</b></li>
<li><b>WBEM_FLAG_CREATE_OR_UPDATE</b></li>
<li><b>WBEM_FLAG_UPDATE_ONLY</b></li>
</ul>

### -param pContext






#### - newInstance [ref]

Instance that is updated.


## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> method lists the most common return values, although you can choose to return any COM return code.




## -remarks



WMI invokes <b>PutInstance</b> when a client calls <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> against your class. You must implement <b>PutInstance</b> if your framework provider updates instances. The following list describes a common implementation of <b>PutInstance</b>:

<ol>
<li>
Examine the key properties passed in by the client with the Get methods for <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>, such as <a href="https://msdn.microsoft.com/d9295ba1-19da-41a2-86d1-ec80e18e895b">CInstance::GetCHString</a>.

Your implementation should determine if your provider supports the changes requested by the client.

</li>
<li>Create or update the appropriate managed object, as necessary.</li>
<li>
Return the appropriate return value.

If your provider does not support the changes requested by the client, you should return an appropriate error code. For a complete listing of valid error codes, see <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>.

</li>
</ol>


