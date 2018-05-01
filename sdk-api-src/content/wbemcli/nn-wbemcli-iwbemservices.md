---
UID: NN:wbemcli.IWbemServices
title: IWbemServices
author: windows-driver-content
description: Used by clients and providers to access WMI services. The interface is implemented by WMI and WMI providers, and is the primary WMI interface.
old-location: wmi\iwbemservices.htm
old-project: WmiSdk
ms.assetid: 58e2ecca-7d1f-4831-93fc-f946f8ada2c0
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWbemServices, IWbemServices interface [Windows Management Instrumentation], IWbemServices interface [Windows Management Instrumentation], described, _hmm_iwbemservices, wbemcli/IWbemServices, wmi.iwbemservices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fastprox.dll
-	Esscli.dll
-	FrameDyn.dll
-	FrameDynOS.dll
-	Ntevt.dll
-	Stdprov.dll
-	Viewprov.dll
-	Wbemcomn.dll
-	Wbemcore.dll
-	Wbemess.dll
-	Wbemsvc.dll
-	Wmipicmp.dll
-	Wmidcprv.dll
-	Wmipjobj.dll
-	Wmiprvsd.dll
api_name:
-	IWbemServices
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices interface


## -description


The <b>IWbemServices</b> interface is used by clients and providers to access WMI services. The interface is implemented by WMI and WMI providers, and is the primary WMI interface.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    IWbemClassObject *pObj = NULL;

    //The pWbemSvc pointer is of type IWbemServices*
    pWbemSvc-&gt;GetObject(L"path", 0, 0, &amp;pObj, 0);</pre>
</td>
</tr>
</table></span></div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/803a7831-1e3d-4940-8d2b-1a74dd16f51a">CancelAsyncCall</a>
</td>
<td align="left" width="63%">
Cancels a currently executing asynchronous call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23122b38-5671-4454-be79-85c6bc34daa0">CreateClassEnum</a>
</td>
<td align="left" width="63%">
Creates a class enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02b81f48-c6a0-44db-86b9-936331b15cc4">CreateClassEnumAsync</a>
</td>
<td align="left" width="63%">
Creates a class enumerator that executes asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47671b9b-a2ff-4375-b2a4-7e8599f1fb69">CreateInstanceEnum</a>
</td>
<td align="left" width="63%">
Creates an instance enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ba2ff28-034f-4949-9bde-8c98345ec7c6">CreateInstanceEnumAsync</a>
</td>
<td align="left" width="63%">
Creates an instance enumerator that executes asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1266d93a-776c-481d-b343-826a5c808d24">DeleteClass</a>
</td>
<td align="left" width="63%">
Deletes a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebb58f3b-201c-4e37-8a51-9b5e2365cf3c">DeleteClassAsync</a>
</td>
<td align="left" width="63%">
Deletes a class and receives confirmation asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">DeleteInstance</a>
</td>
<td align="left" width="63%">
Deletes a specific instance of a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c726842-a274-41d1-b622-681bf9f6ae8b">DeleteInstanceAsync</a>
</td>
<td align="left" width="63%">
Deletes an instance and provides confirmation asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">ExecMethod</a>
</td>
<td align="left" width="63%">
Executes an object method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61966c03-80dc-4556-b2fc-97e879cf458c">ExecMethodAsync</a>
</td>
<td align="left" width="63%">
Executes an object method asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe547660-4095-4a75-829d-f06599c0d9d7">ExecNotificationQuery</a>
</td>
<td align="left" width="63%">
Executes a query to receive events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f26eb44a-e0c4-418b-b849-d38d85ef236a">ExecNotificationQueryAsync</a>
</td>
<td align="left" width="63%">
Executes a query to receive events asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a">ExecQuery</a>
</td>
<td align="left" width="63%">
Executes a query to retrieve classes or instances.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8b55500-d84c-431b-93c6-99d1f1b845c3">ExecQueryAsync</a>
</td>
<td align="left" width="63%">
Executes a query to retrieve classes or instances asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an object—an instance or class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6868a14d-3776-43a0-b241-b40d42a97afc">GetObjectAsync</a>
</td>
<td align="left" width="63%">
Asynchronously retrieves an object—an instance or class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09ff9078-3d97-432b-8626-62f12b5e3ef4">OpenNamespace</a>
</td>
<td align="left" width="63%">
Opens a specific child namespace for operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">PutClass</a>
</td>
<td align="left" width="63%">
Creates or updates a class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/957f5646-86e7-4632-9012-b1fb281b65fb">PutClassAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates or updates a class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">PutInstance</a>
</td>
<td align="left" width="63%">
Creates or updates an instance of a specific class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fef3eb72-74ba-49cd-b992-292405d29917">PutInstanceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates or updates an instance of a specific class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/218b42f2-838d-4d8f-98d2-9334ec29d279">QueryObjectSink</a>
</td>
<td align="left" width="63%">
Allows a caller to obtain a notification handler sink.

</td>
</tr>
</table> 


## -remarks



Providers that implement the 
<b>IWbemServices</b> interface must follow the documented semantics of each method that they implement; and providers must support the specified error return codes. WMI implements all of the methods, and typically, each provider implements a small subset of the available functionality on the interface. Providers must return WBEM_E_PROVIDER_NOT_CAPABLE for any method that  they do not implement.

All outbound interface pointers from any 
<b>IWbemServices</b> method should be initialized to <b>NULL</b> before calling the interface method. For example, 
calls to the <a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a> method return an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interface pointer that should be pre-initialized to <b>NULL</b> before the <b>IWbemServices::GetObject</b> method  call.


#### Examples

For multiple C++ examples that use IWbemServices, see the <a href="https://msdn.microsoft.com/5c4c4c4c-adbc-4702-a6fe-5f98a6db3ba1">WMI C++ Application Examples</a> section.

The following code example shows how a provider can get an 
<b>IWbemServices</b> pointer. The code requires the following #include statements and references to compile.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;iostream&gt;
using namespace std;
#include &lt;wbemidl.h&gt;
#pragma comment(lib, "wbemuuid.lib")</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IWbemLocator *pIWbemLocator = NULL;

HRESULT hRes = CoCreateInstance (
            CLSID_WbemAdministrativeLocator,
            NULL ,
            CLSCTX_INPROC_SERVER | CLSCTX_LOCAL_SERVER , 
            IID_IUnknown ,
            ( void ** ) &amp;pIWbemLocator
            ) ;

IWbemServices *pWbemServices = NULL;

if (SUCCEEDED(hRes))
{
    hRes = pIWbemLocator-&gt;ConnectServer(
                L"root\\CIMV2",  // Namespace
                NULL,          // Userid
                NULL,           // PW
                NULL,           // Locale
                0,              // flags
                NULL,           // Authority
                NULL,           // Context
                &amp;pWbemServices
                );

pIWbemLocator-&gt;Release(); // Free memory resources.

// Use pWbemServices

}

// Clean up
pWbemServices-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/87bc5d10-a5d7-444b-b823-4e1a2d63efb3">Creating WMI Providers</a>



<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>



<a href="https://msdn.microsoft.com/919dfa7c-4a36-4e59-8377-72cf9735eaec">Supplying Data to WMI by Writing a Provider</a>
 

 

