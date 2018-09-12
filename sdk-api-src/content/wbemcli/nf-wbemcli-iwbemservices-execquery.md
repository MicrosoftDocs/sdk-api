---
UID: NF:wbemcli.IWbemServices.ExecQuery
title: IWbemServices::ExecQuery
author: windows-sdk-content
description: The IWbemServices::ExecQuery method executes a query to retrieve objects.
old-location: wmi\iwbemservices_execquery.htm
tech.root: WmiSdk
ms.assetid: 8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ExecQuery, ExecQuery method [Windows Management Instrumentation], ExecQuery method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecQuery method, IWbemServices.ExecQuery, IWbemServices::ExecQuery, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_ENSURE_LOCATABLE, WBEM_FLAG_FORWARD_ONLY, WBEM_FLAG_PROTOTYPE, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_execquery, wbemcli/IWbemServices::ExecQuery, wmi.iwbemservices_execquery
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
 - IWbemServices.ExecQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemServices::ExecQuery


## -description


The 
<b>IWbemServices::ExecQuery</b> method executes a query to retrieve objects.

For the valid types of queries that can be performed, see 
<a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a>.


## -parameters




### -param strQueryLanguage [in]

Valid <b>BSTR</b> that contains one of the query languages supported by Windows Management. This must be "WQL", the acronym for WMI Query Language.


### -param strQuery [in]

Valid <b>BSTR</b> that contains the text of the query. This parameter cannot be <b>NULL</b>. For more information on building WMI query strings, see <a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a> and the <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL</a> reference.


### -param lFlags [in]

The following flags affect the behavior of this method. The suggested value for this parameter is <b>WBEM_FLAG_RETURN_IMMEDIATELY</b> and <b>WBEM_FLAG_FORWARD_ONLY</b> for best performance.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_FORWARD_ONLY

This flag causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators but do not allow calls to 
<a href="https://msdn.microsoft.com/a323c662-e005-44aa-a903-1eb7d6ddff9e">Clone</a> or 
<a href="https://msdn.microsoft.com/571b7067-676f-4e9e-9694-268ec10dc60b">Reset</a>.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes Windows Management to retain pointers to objects of the enumeration until the client releases the enumerator.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag causes this to be a semisynchronous call. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.



#### WBEM_FLAG_ENSURE_LOCATABLE

This flag ensures that any returned objects have enough information in them so that the system properties, such as <b>__PATH</b>, <b>__RELPATH</b>, and <b>__SERVER</b>, are non-NULL.



#### WBEM_FLAG_PROTOTYPE

This flag is used for prototyping. It does not execute the query and instead returns an object that looks like a typical result object.



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without any regard to its parent class or subclasses.


### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that can be used by the provider that is providing the requested classes or instances. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param ppEnum [out]

If no error occurs, this receives the enumerator that allows the caller to retrieve the instances in the result set of the query. It is not an error for the query to have a result set with 0 instances. This is determined only by attempting to iterate through the instances. This object returns with a positive reference count. The caller must call <a href="_com_iunknown_release">Release</a> when the object is no longer required.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a>.

COM-specific error codes also can be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



The 
<b>IWbemServices::ExecQuery</b> method processes the query specified in the <i>strQuery</i> parameter and creates an enumerator through which the caller can access the query results. The enumerator is a pointer to an 
<a href="https://msdn.microsoft.com/142ea48d-d47b-4b7b-ab84-049a54955488">IEnumWbemClassObject</a> interface; the query results are instances of class objects made available through the 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interface.

There are limits to the number of "AND" and "OR" keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the <b>WBEM_E_QUOTA_VIOLATION</b> error code as an <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.




## -see-also




<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/d8b55500-d84c-431b-93c6-99d1f1b845c3">IWbemServices::ExecQueryAsync</a>



<a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a>
 

 

