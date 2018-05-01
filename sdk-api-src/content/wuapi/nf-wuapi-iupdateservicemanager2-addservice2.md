---
UID: NF:wuapi.IUpdateServiceManager2.AddService2
title: IUpdateServiceManager2::AddService2 method
author: windows-driver-content
description: Registers a service with Windows Update Agent (WUA) without requiring an authorization cabinet file (.cab). This method also returns a pointer to an IUpdateServiceRegistration interface.
old-location: wua\iupdateservicemanager2_addservice2_methods.htm
old-project: Wua_Sdk
ms.assetid: 1584b92f-ba21-4b03-a1b4-540313eb7893
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: AddService2 method [Windows Update Agent], AddService2 method [Windows Update Agent], IUpdateServiceManager2 interface, AddService2,IUpdateServiceManager2.AddService2, IUpdateServiceManager2, IUpdateServiceManager2 interface [Windows Update Agent], AddService2 method, IUpdateServiceManager2::AddService2, wua.iupdateservicemanager2_addservice2_methods, wuapi/IUpdateServiceManager2::AddService2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdateServiceManager2.AddService2
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateServiceManager2::AddService2 method


## -description


Registers a service with Windows Update Agent (WUA) without requiring an authorization cabinet file (.cab). This method also  returns a pointer to an <a href="https://msdn.microsoft.com/ae742fe2-c9f3-4116-b98a-3cf3906cfda2">IUpdateServiceRegistration</a> interface.


## -parameters




### -param serviceID [in]

An identifier for the service to be registered.


### -param flags [in]

A combination of <a href="https://msdn.microsoft.com/1372a062-9f62-4b4d-8476-b6c7059a801a">AddServiceFlag</a> values that are combined by using a bitwise OR operation. The resulting value specifies options for service registration. For more info, see Remarks. 


### -param authorizationCabPath [in]

The path of the Microsoft signed local cabinet file (.cab) that has the information that is required for a service registration.  If empty, the update agent searches for the authorization cabinet file (.cab) during service registration when a network connection is available.


### -param retval [out]

A pointer to an <a href="https://msdn.microsoft.com/729664f2-5f75-4e73-9ccc-150b2e201f66">IUpdateServiceRegistration</a> interface that represents an added service.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This method cannot be called from a remote computer if the <i>authorizationCabPath</i> parameter is set to a null string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DS_SERVICEEXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The authorization cabinet file (.cab) has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DS_INVALIDOPERATION</b></dt>
</dl>
</td>
<td width="60%">
The state of Automatic Updates could not be changed.

</td>
</tr>
</table>
 




## -remarks



This method may return <a href="https://msdn.microsoft.com/07ff2ed7-09bc-4af7-84f9-66a921c0f53f">networking error codes</a> when the <b>asfAllowOnlineRegistration</b> flag is specified.

The <i>authorizationCabPath</i> parameter is optional for this method. If the <i>authorizationCabPath</i> parameter is not specified, it will be retrieved from the Windows Update server.

This method returns <b>E_INVALIDARG</b> if the <b>asfAllowOnlineRegistration</b> or <b>asfAllowPendingRegistration</b> flags are specified and if the value of the <i>authorizationCabPath</i> parameter is not an empty string.

This method returns <b>WU_E_DS_INVALIDOPERATION</b> if the requested change in the state of Automatic Updates is contrary to the specifications in the authorization cabinet file (.cab) when the <b>asfRegisterServiceWithAU</b> flag is specified. An error is returned by the <a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> function if the authorization cabinet file has not been signed.

The update agent and <b>AddService2</b> behave in the following ways depending on the <a href="https://msdn.microsoft.com/1372a062-9f62-4b4d-8476-b6c7059a801a">AddServiceFlag</a> values that you specify in the <i>flags</i> parameter:

<ul>
<li>If you specify <b>asfAllowOnlineRegistration</b> without <b>asfAllowPendingRegistration</b>, the update agent immediately attempts to go online to register the service. <b>AddService2</b> returns an HRESULT value that reflects the success or failure of the registration. If the registration fails, the update agent makes no future attempts to register the service.</li>
<li>If you specify <b>asfAllowPendingRegistration</b> without <b>asfAllowOnlineRegistration</b>, the update agent doesn't register the service immediately. <b>AddService2</b> returns  S_OK to indicate that the update agent will attempt to register the service at a later time, which doesn't guarantee that the registration will eventually succeed.</li>
<li>If you specify <b>asfAllowPendingRegistration</b> and <b>asfAllowOnlineRegistration</b> together, the update agent immediately attempts to go online to register the service. <b>AddService2</b> returns S_OK if the registration succeeds. <b>AddService2</b> returns a failure HRESULT value if the registration fails, but the update agent still attempts to register the service at a later time.</li>
<li>If you specify <b>asfAllowPendingRegistration</b>, <b>asfAllowOnlineRegistration</b>, or both, also specify <b>NULL</b> for the <i>authorizationCabPath</i> parameter.</li>
<li>If you specify neither <b>asfAllowPendingRegistration</b> nor <b>asfAllowOnlineRegistration</b> (in other words, if <i>flags</i> is either zero or <b>asfRegisterServiceWithAU</b>), you must specify a non-<b>NULL</b> path in the <i>authorizationCabPath</i> parameter. In this mode, <b>AddService2</b> processes the cabinet file (.cab) and registers the service in the same way as <a href="https://msdn.microsoft.com/b4071ef7-316f-4624-bc43-79c5982c4a82">IUpdateServiceManager::AddService</a>.</li>
<li>If you specify <b>asfRegisterServiceWithAU</b>, the change to the default Automatic Updates service doesn't occur (and isn't reflected in the Windows Update user interface) until the service registration succeeds. This means that if the registration succeeds immediately (because you specified <b>asfAllowPendingRegistration</b> or supplied  a cabinet file (.cab)), the Automatic Updates service change also occurs immediately. If the registration doesn't succeed until later (because you specified <b>asfAllowPendingRegistration</b>), the Automatic Updates service change doesn't occur unless the pending service registration eventually succeeds.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/26b75edc-eb43-4ee0-8040-da8b3252cf21">IUpdateServiceManager2</a>
 

 

