---
UID: NF:wbemcli.IWbemServices.PutClass
title: IWbemServices::PutClass
author: windows-sdk-content
description: The IWbemServices::PutClass method creates a new class or updates an existing one. The class specified by the pObject parameter must have been correctly initialized with all of the required property values.
old-location: wmi\iwbemservices_putclass.htm
tech.root: WmiSdk
ms.assetid: fcb8694e-6bf1-426d-bc1d-18cf9925f1e0
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IWbemServices interface [Windows Management Instrumentation],PutClass method, IWbemServices.PutClass, IWbemServices::PutClass, PutClass, PutClass method [Windows Management Instrumentation], PutClass method [Windows Management Instrumentation],IWbemServices interface, WBEM_FLAG_CREATE_ONLY, WBEM_FLAG_CREATE_OR_UPDATE, WBEM_FLAG_OWNER_UPDATE, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_UPDATE_COMPATIBLE, WBEM_FLAG_UPDATE_FORCE_MODE, WBEM_FLAG_UPDATE_ONLY, WBEM_FLAG_UPDATE_SAFE_MODE, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_putclass, wbemcli/IWbemServices::PutClass, wmi.iwbemservices_putclass
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
 - IWbemServices.PutClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemServices::PutClass


## -description


The 
<b>IWbemServices::PutClass</b> method creates a new class or updates an existing one. The class specified by the <i>pObject</i> parameter must have been correctly initialized with all of the required property values.

The user may not create classes with names that begin or end with an underscore (_). This is reserved for system classes.


## -parameters




### -param pObject [in]

Must point to a valid class definition. The reference count is not changed.


### -param lFlags [in]

The following flags affect the behavior of this method.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI does not store any qualifiers with the amended flavor. If this flag is not set, it is assumed that this object is not localized, and all qualifiers are stored with this instance.



#### WBEM_FLAG_CREATE_OR_UPDATE

This flag causes the class to be created if it does not exist, or overwritten if it exists already.



#### WBEM_FLAG_UPDATE_ONLY

This flag causes this call to update. The class must exist for the call to be successful.



#### WBEM_FLAG_CREATE_ONLY

This flag is used for creation only. The call fails if the class already exists.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes this to be a semisynchronous call. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.



#### WBEM_FLAG_OWNER_UPDATE

Push providers must specify this flag when calling 
<b>PutClass</b>, to indicate that this class has changed.



#### WBEM_FLAG_UPDATE_COMPATIBLE

This flag allows a class to be updated if there are no derived classes and there are no instances for that class. It also allows updates in all cases if the change is just to nonimportant qualifiers (for example, the <b>Description</b> qualifier). This is the default behavior for this call and is used for compatibility with previous versions of Windows Management. If the class has instances or changes are to important qualifiers, the update fails.



#### WBEM_FLAG_UPDATE_SAFE_MODE

This flag allows updates of classes even if there are child classes as long as the change does not cause any conflicts with child classes. An example of an update this flag would allow would be to add a new property to the base class that was not previously mentioned in any of the child classes. If the class has instances, the update fails.



#### WBEM_FLAG_UPDATE_FORCE_MODE

This flag forces updates of classes when conflicting child classes exist. An example of an update this flag would force would be if a class qualifier were defined in a child class, and the base class tried to add the same qualifier which conflicted with the existing one. In force mode, this conflict would be resolved by deleting the conflicting qualifier in the child class.


### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object required by the dynamic class provider that is producing the class instances. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param ppCallResult [out]

If <b>NULL</b>, this parameter is not used. If the <i>lFlags</i> parameter contains <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, this call returns immediately with <b>WBEM_S_NO_ERROR</b>. The <i>ppCallResult</i> parameter receives a pointer to a new 
<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a> object, which can then be polled to obtain the result using the 
<a href="https://msdn.microsoft.com/5a600fd8-87d8-446d-93da-5b22fd575a11">IWbemCallResult::GetCallStatus</a> method.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

<div class="alert"><b>Note</b>  Unpredictable behavior will result if you change class definitions while they are in use by clients or providers. The 
<b>IWbemServices::PutClass</b> method should only be used to create or update a class when there are no clients or providers currently using the class.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/06b75910-f126-48b6-8e43-4a9ed4661732">Creating a Class</a>



<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/f54b8e7c-c531-47d5-bab8-780652b94555">Retrieving an Error Code</a>
 

 

