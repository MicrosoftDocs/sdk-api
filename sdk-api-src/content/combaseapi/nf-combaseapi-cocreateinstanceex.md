---
UID: NF:combaseapi.CoCreateInstanceEx
title: CoCreateInstanceEx function
author: windows-driver-content
description: Creates an instance of a specific class on a specific computer.
old-location: com\cocreateinstanceex.htm
old-project: com
ms.assetid: 3b414b95-e8d2-42e8-b4f2-5cc5189a3d08
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CoCreateInstanceEx, CoCreateInstanceEx function [COM], _com_CoCreateInstanceEx, com.cocreateinstanceex, combaseapi/CoCreateInstanceEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REGCLS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	API-MS-Win-Core-Com-l1-1-0.dll
-	ComBase.dll
-	API-MS-Win-Core-Com-l1-1-1.dll
-	API-MS-Win-DownLevel-Ole32-l1-1-0.dll
-	API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
-	CoCreateInstanceEx
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoCreateInstanceEx function


## -description


Creates an instance of a specific class on a specific computer.


## -parameters




### -param Clsid

TBD


### -param punkOuter [in]

If this parameter non-<b>NULL</b>, indicates the instance is being created as part of an aggregate, and <i>punkOuter</i> is to be used as the new instance's controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. Aggregation is currently not supported cross-process or cross-computer. When instantiating an object out of process, CLASS_E_NOAGGREGATION will be returned if <i>punkOuter</i> is non-<b>NULL</b>.


### -param dwClsCtx [in]

A value from the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration.


### -param pServerInfo [in]

Information about the computer on which to instantiate the object. See <a href="https://msdn.microsoft.com/88c94a7f-5cf0-4d61-833f-91cba45d8624">COSERVERINFO</a>. This parameter can be <b>NULL</b>, in which case the object is instantiated on the local computer or at the computer specified in the registry under the class's <a href="https://msdn.microsoft.com/0413564e-e8ba-4e6e-ad29-62997c63aab3">RemoteServerName</a> value, according to the interpretation of the <i>dwClsCtx</i> parameter.


### -param dwCount [in]

The number of structures in <i>pResults</i>. This value must be greater than 0.


### -param pResults [in, out]

An array of <a href="https://msdn.microsoft.com/845040c9-fad4-4ac8-856d-d35edbf48ec9">MULTI_QI</a> structures. Each structure has three members: the identifier for a requested interface (<b>pIID</b>), the location to return the interface pointer (<b>pItf</b>) and the return value of the call to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> (<b>hr</b>).


#### - rclsid [in]

The CLSID of the object to be created.


## -returns



This function can return the standard return value E_INVALIDARG, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
A specified class is not registered in the registration database. Also can indicate that the type of server you requested in the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration is not registered or the values for the server types in the registry are corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLASS_E_NOAGGREGATION</b></dt>
</dl>
</td>
<td width="60%">
This class cannot be created as part of an aggregate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_S_NOTALLINTERFACES</b></dt>
</dl>
</td>
<td width="60%">
At least one, but not all of the interfaces requested in the <i>pResults</i> array were successfully retrieved. The <b>hr</b> member of each of the <a href="https://msdn.microsoft.com/845040c9-fad4-4ac8-856d-d35edbf48ec9">MULTI_QI</a> structures in <i>pResults</i> indicates with S_OK or E_NOINTERFACE whether the specific interface was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
None of the interfaces requested in the <i>pResults</i> array were successfully retrieved.

</td>
</tr>
</table>
 




## -remarks



<b>CoCreateInstanceEx</b> creates a single uninitialized object associated with the given CLSID on a specified remote computer. This is an extension of the function <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>, which creates an object on the local computer only. In addition, rather than requesting a single interface and obtaining a single pointer to that interface, <b>CoCreateInstanceEx</b> makes it possible to specify an array of structures, each pointing to an interface identifier (IID) on input, and, on return, containing (if available) a pointer to the requested interface and the return value of the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call for that interface. This permits fewer round trips between computers.

This function encapsulates three calls: first, to <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> to connect to the class object associated with the specified CLSID, specifying the location of the class; second, to <a href="https://msdn.microsoft.com/45d34150-9e0b-4a76-a784-c81434ec73b8">IClassFactory::CreateInstance</a> to create an uninitialized instance, and finally, to <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IClassFactory::Release</a>, to release the class object. 



The object so created must still be initialized through a call to one of the initialization interfaces (such as <a href="https://msdn.microsoft.com/34379b8d-4e00-49cd-9fd1-65f88746c61a">IPersistStorage::Load</a>). Two functions, <a href="https://msdn.microsoft.com/f8a22f5f-a21f-49e7-bd6c-ca987206ee46">CoGetInstanceFromFile</a> and <a href="https://msdn.microsoft.com/6a77770c-b7e1-4d29-9c4b-331b5950a635">CoGetInstanceFromIStorage</a> encapsulate both the instance creation and initialization from the obvious sources.

The <a href="https://msdn.microsoft.com/88c94a7f-5cf0-4d61-833f-91cba45d8624">COSERVERINFO</a> structure passed as the <i>pServerInfo</i> parameter contains the security settings that COM will use when creating a new instance of the specified object. Note that this parameter does not influence the security settings used when making method calls on the instantiated object. Those security settings are configurable, on a per-interface basis, with the <a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a> function. Also see, <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a>.





## -see-also




<a href="https://msdn.microsoft.com/f8a22f5f-a21f-49e7-bd6c-ca987206ee46">CoGetInstanceFromFile</a>



<a href="https://msdn.microsoft.com/6a77770c-b7e1-4d29-9c4b-331b5950a635">CoGetInstanceFromIStorage</a>
 

 

