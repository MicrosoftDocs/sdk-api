---
UID: NF:wbemcli.IWbemServices.PutInstance
title: IWbemServices::PutInstance (wbemcli.h)
description: The IWbemServices::PutInstance method creates or updates an instance of an existing class. The instance is written to the WMI repository.
helpviewer_keywords: ["IWbemServices interface [Windows Management Instrumentation]","PutInstance method","IWbemServices.PutInstance","IWbemServices::PutInstance","PutInstance","PutInstance method [Windows Management Instrumentation]","PutInstance method [Windows Management Instrumentation]","IWbemServices interface","WBEM_FLAG_CREATE_ONLY","WBEM_FLAG_CREATE_OR_UPDATE","WBEM_FLAG_RETURN_IMMEDIATELY","WBEM_FLAG_UPDATE_ONLY","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_putinstance","wbemcli/IWbemServices::PutInstance","wmi.iwbemservices_putinstance"]
old-location: wmi\iwbemservices_putinstance.htm
tech.root: wmi
ms.assetid: 1e07b328-40f7-4e14-bf53-9a5cebfc23f6
ms.date: 12/05/2018
ms.keywords: IWbemServices interface [Windows Management Instrumentation],PutInstance method, IWbemServices.PutInstance, IWbemServices::PutInstance, PutInstance, PutInstance method [Windows Management Instrumentation], PutInstance method [Windows Management Instrumentation],IWbemServices interface, WBEM_FLAG_CREATE_ONLY, WBEM_FLAG_CREATE_OR_UPDATE, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_UPDATE_ONLY, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_putinstance, wbemcli/IWbemServices::PutInstance, wmi.iwbemservices_putinstance
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemServices::PutInstance
 - wbemcli/IWbemServices::PutInstance
dev_langs:
 - c++
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
 - IWbemServices.PutInstance
---

# IWbemServices::PutInstance


## -description

The 
<b>IWbemServices::PutInstance</b> method creates or updates an instance of an existing class. The instance is written to the WMI repository.

## -parameters

### -param pInst [in]

Pointer to the instance to be written. The caller cannot make assumptions about the reference count at the completion of this call.

### -param lFlags [in]

One or more of the following values can be set.



#### WBEM_FLAG_CREATE_OR_UPDATE

This flag causes the instance to be created if it does not exist or overwritten if it exists already.



#### WBEM_FLAG_UPDATE_ONLY

This flag causes this call to update. The instance must exist for the call to be successful.



#### WBEM_FLAG_CREATE_ONLY

This flag is used for creation only. The call fails if the instance already exists.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes this to be a semisynchronous call. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI does not store any qualifiers with the <b>Amended</b> flavor. If this flag is not set, it is assumed that this object is not localized, and all qualifiers are stored with this instance.

### -param pCtx [in]

Typically <b>NULL</b>, indicating that every property in the instance is to be updated. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object containing more information about the instance. The data in the context object must be documented by the provider responsible for the instance. A non-<b>NULL</b><b>IWbemContext</b> object can indicate whether support exists for partial-instance updates.

For more information about how to support full and partial-instance updates, see 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync">IWbemServices::PutInstanceAsync</a>. For more information about requesting a full or partial-instance update operation, see 
<a href="/windows/desktop/WmiSdk/modifying-an-instance-property">Modifying an Instance Property</a>.

### -param ppCallResult [out]

If <b>NULL</b>, this parameter is not used. If the <i>lFlags</i> parameter contains <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, this call returns immediately with <b>WBEM_S_NO_ERROR</b>. The <i>ppCallResult</i> parameter then receives a pointer to a new 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a> object, which can be polled with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus">IWbemCallResult::GetCallStatus</a> to obtain the result.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

Applications and providers call 
<b>PutInstance</b> to create or update an instance of an existing class. Depending on how the <i>pCtx</i> parameter is set, either some or all of the properties of the instance are updated. For more information about how to support partial instance updating, see 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync">IWbemServices::PutInstanceAsync</a>. For more information about requesting a partial instance update, see 
<a href="/windows/desktop/WmiSdk/modifying-an-instance-property">Modifying an Instance Property</a>.

The 
<b>PutInstance</b> method supports creating instances and updating instances only. It does not support moving instances. That is, a caller cannot set the <i>pInst</i> parameter to an instance that has a key that is the same as another instance in a sibling class. For example, suppose <b>ClassA</b> is the base class to <b>ClassB</b> and <b>ClassC</b>. The <b>ClassA</b> class defines the <b>KeyProp</b> property as its key and <b>ClassB</b> has an instance that has <b>KeyProp</b> set to 1. To create an instance of <b>ClassC</b> with <b>KeyProp</b> set to 1, an application must first delete the <b>ClassB</b> instance by calling 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">DeleteInstance</a> and then save the <b>ClassC</b> instance with 
<b>PutInstance</b>.

When the instance pointed to by <i>pInst</i> belongs to a subclass, Windows Management calls all of the providers responsible for the classes from which the subclass derives. All of these providers must succeed for the original 
<b>PutInstance</b> request to succeed. The provider supporting the topmost class in the hierarchy is called first. The calling order continues with the subclass of the topmost class and proceeds from top to bottom until Windows Management reaches the provider for the class owning the instance pointed to by <i>pInst</i>.

Windows Management does not call the providers for any of the child classes of an instance. Therefore, if an application wants to change the values of inherited properties, the application must call 
<b>PutInstance</b> on the full instance of the child class rather than a corresponding instance of the parent class.

When an application must update an instance that belongs to a class hierarchy, the <i>pInst</i> parameter must point to the instance containing the properties to be modified. That is, consider a target instance that belongs to <b>ClassB</b>. The <b>ClassB</b> instance derives from <b>ClassA</b>, and <b>ClassA</b> defines the property <b>PropA</b>. If an application wants to make a change to the value of <b>PropA</b> in the <b>ClassB</b> instance, it must set <i>pInst</i> to that instance rather than an instance of <b>ClassA</b>.

Calling 
<b>PutInstance</b> on an instance of an abstract class is not allowed.

## -see-also

<a href="/windows/desktop/WmiSdk/creating-an-instance">Creating an Instance</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync">IWbemServices::PutInstanceAsync</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>