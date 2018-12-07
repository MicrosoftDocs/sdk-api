---
UID: NF:wbemcli.IWbemServices.DeleteInstance
title: IWbemServices::DeleteInstance
author: windows-sdk-content
description: The IWbemServices::DeleteInstance method deletes an instance of an existing class in the current namespace.
old-location: wmi\iwbemservices_deleteinstance.htm
tech.root: WmiSdk
ms.assetid: f6dfeb1d-1730-4df4-adf7-f27dd9edc54d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteInstance, DeleteInstance method [Windows Management Instrumentation], DeleteInstance method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],DeleteInstance method, IWbemServices.DeleteInstance, IWbemServices::DeleteInstance, WBEM_FLAG_RETURN_IMMEDIATELY, _hmm_iwbemservices_deleteinstance, wbemcli/IWbemServices::DeleteInstance, wmi.iwbemservices_deleteinstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Esscli.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Ntevt.dll
 - Stdprov.dll
 - Viewprov.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wbemsvc.dll
 - Wmipicmp.dll
 - Wmidcprv.dll
 - Wmipjobj.dll
 - Wmiprvsd.dll
api_name:
 - IWbemServices.DeleteInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemServices::DeleteInstance


## -description


The 
<b>IWbemServices::DeleteInstance</b> method deletes an instance of an existing class in the current namespace.


## -parameters




### -param strObjectPath [in]

Valid <b>BSTR</b> containing the object path to the instance to be deleted.


### -param lFlags [in]

One of the following values are valid.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes this to be a semisynchronous call. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


### -param pCtx [in]

Typically NULL. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that may be used by the provider that is deleting the instance. The values in the context object must be specified in the documentation for the provider in question.


### -param ppCallResult [out]

If NULL, this parameter is not used. If <i>ppCallResult</i> is specified, it must be set to point to <b>NULL</b> on entry. If the <i>lFlags</i> parameter contains <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, this call returns immediately with <b>WBEM_S_NO_ERROR</b>. The <i>ppCallResult</i> parameter receives a pointer to a new 
<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a> object, which can then be polled to obtain the result using the 
<a href="https://msdn.microsoft.com/5a600fd8-87d8-446d-93da-5b22fd575a11">GetCallStatus</a> method.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



The 
<b>IWbemServices::DeleteInstance</b> method is called to delete an existing instance in the current namespace. Instances in other namespaces cannot be deleted. When 
<b>DeleteInstance</b> is called to delete an instance that belongs to a class in a hierarchy, Windows Management calls the 
<a href="https://msdn.microsoft.com/7c726842-a274-41d1-b622-681bf9f6ae8b">DeleteInstanceAsync</a> method for all of the providers responsible for non-abstract classes in the hierarchy. That is, if the <i>strObjectPath</i> parameter identifies an instance of ClassB, and ClassB derives from ClassA, a non-abstract class, and is the parent class of ClassC and ClassD, also non-abstract classes, the providers for all four classes are called.

Windows Management calls each provider with an object path that is modified to point to their class. For example, if <i>strObjectPath</i> for the original call is set to "ClassB.k=1", the call to the provider of ClassA would set <i>strObjectPath</i> to "ClassA.k=1".

The success of a 
<b>DeleteInstance</b> call depends only on the success of a 
<a href="https://msdn.microsoft.com/7c726842-a274-41d1-b622-681bf9f6ae8b">DeleteInstanceAsync</a> call to the provider of the topmost non-abstract class. A non-abstract class has an abstract class as its parent. If the provider for any one of such classes succeeds, the operation succeeds; if all such classes fail, the operation fails.

For example, assume that ClassX is the base class for the following hierarchy:

<ol>
<li>ClassA derives from ClassX.</li>
<li>ClassB derives from ClassA.</li>
<li>ClassC and ClassD derive from ClassB.</li>
</ol>
If ClassX is the only abstract class in the hierarchy and the <i>strObjectPath</i> parameter in 
<b>DeleteInstance</b> points to an instance of ClassB, only the provider for ClassA needs to succeed in its 
<a href="https://msdn.microsoft.com/7c726842-a274-41d1-b622-681bf9f6ae8b">DeleteInstanceAsync</a> call.

If ClassX, ClassA, and ClassB are all abstract and the <i>strObjectPath</i> parameter in 
<b>DeleteInstance</b> again points to an instance of ClassB, either the provider for ClassC or the provider for ClassD must succeed.




## -see-also




<a href="https://msdn.microsoft.com/78a194f0-cd21-4622-9242-be7e430b96c0">Describing an Instance Object Path</a>



<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/7c726842-a274-41d1-b622-681bf9f6ae8b">IWbemServices::DeleteInstanceAsync</a>



<a href="https://msdn.microsoft.com/f54b8e7c-c531-47d5-bab8-780652b94555">Retrieving an Error Code</a>
 

 

