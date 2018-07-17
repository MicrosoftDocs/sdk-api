---
UID: NF:combaseapi.CoCreateInstanceFromApp
title: CoCreateInstanceFromApp function
author: windows-sdk-content
description: Creates an instance of a specific class on a specific computer from within an app container.
old-location: com\cocreateinstancefromapp.htm
old-project: com
ms.assetid: 1C773D78-5B33-44FE-A09B-AB8087F678A1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CoCreateInstanceFromApp, CoCreateInstanceFromApp function [COM], com.cocreateinstancefromapp, combaseapi/CoCreateInstanceFromApp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - combase.dll
 - API-MS-Win-Core-COM-l1-1-0.dll
 - API-MS-Win-Core-COM-l1-1-1.dll
api_name:
 - CoCreateInstanceFromApp
product: Windows
targetos: Windows
req.lib: Combase.lib
req.dll: Combase.dll
req.irql: 
---

# CoCreateInstanceFromApp function


## -description


Creates an instance of a specific class on a specific computer from within an app container.


## -parameters




### -param Clsid

TBD


### -param punkOuter [in, optional]

If this parameter non-<b>NULL</b>, indicates the instance is being created as part of an aggregate, and <i>punkOuter</i> is to be used as the new instance's controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. Aggregation is currently not supported cross-process or cross-computer. When instantiating an object out of process, CLASS_E_NOAGGREGATION will be returned if <i>punkOuter</i> is non-<b>NULL</b>.


### -param dwClsCtx [in]

A value from the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration.


### -param reserved [in, optional]

Reserved for future use.


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
A specified class is not registered in the registration database, or the class is not supported in the app container. Also can indicate that the type of server you requested in the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration is not registered or the values for the server types in the registry are corrupt. 

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



The <b>CoCreateInstanceFromApp</b> function is the same as the  <a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a> function, with the following differences.


<ul>
<li>The <b>CoCreateInstanceFromApp</b> function reads class registrations only from application contexts, and from the HKLM\SOFTWARE\Classes\CLSID registry hive.</li>
<li>Only built-in classes that are supported in the app container are supplied. Attempts to activate unsupported classes, including all classes installed by 3rd-party code as well as many Windows classes, result in error code <b>REGDB_E_CLASSNOTREG</b>.</li>
<li>The <b>CoCreateInstanceFromApp</b> function is available to Windows Store apps. Desktop applications can call this function, but they have the same restrictions as Windows Store apps.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>



<a href="http://msdn.microsoft.com/en-us/library/ms404523.aspx">Fusion (Unmanaged API Reference)</a>
 

 

