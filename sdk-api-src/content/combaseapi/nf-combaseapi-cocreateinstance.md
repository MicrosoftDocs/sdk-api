---
UID: NF:combaseapi.CoCreateInstance
title: CoCreateInstance function
author: windows-sdk-content
description: Creates a single uninitialized object of the class associated with a specified CLSID.
old-location: com\cocreateinstance.htm
tech.root: com
ms.assetid: 7295a55b-12c7-4ed0-a7a4-9ecee16afdec
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CoCreateInstance, CoCreateInstance function [COM], _com_CoCreateInstance, com.cocreateinstance, combaseapi/CoCreateInstance
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoCreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoCreateInstance function


## -description


Creates a single uninitialized object of the class associated with a specified CLSID.

Call <b>CoCreateInstance</b> when you want to create only one object on the local system. To create a single object on a remote system, call the <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. To create multiple objects based on a single CLSID, call the <a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a> function.


## -parameters




### -param rclsid [in]

The CLSID associated with the data and code that will be used to create the object.


### -param pUnkOuter [in]

If <b>NULL</b>, indicates that the object is not being created as part of an aggregate. If non-<b>NULL</b>, pointer to the aggregate object's <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface (the controlling <b>IUnknown</b>).


### -param dwClsContext [in]

Context in which the code that manages the newly created object will run. The values are taken from the enumeration <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>.


### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the object.


### -param ppv [out]

Address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppv</i> contains the requested interface pointer. Upon failure, *<i>ppv</i> contains <b>NULL</b>.


## -returns



This function can return the following values.

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
An instance of the specified object class was successfully created.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The specified class does not implement the requested interface, or the controlling <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> does not expose the requested interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppv</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <b>CoCreateInstance</b> function provides a convenient shortcut by connecting to the class object associated with the specified CLSID, creating an uninitialized instance, and releasing the class object. As such, it encapsulates the following functionality:

<pre class="syntax" xml:space="preserve"><code>CoGetClassObject(rclsid, dwClsContext, NULL, IID_IClassFactory, &amp;pCF); 
hresult = pCF-&gt;CreateInstance(pUnkOuter, riid, ppvObj) 
pCF-&gt;Release(); 
</code></pre>
It is convenient to use <b>CoCreateInstance</b> when you need to create only a single instance of an object on the local machine. If you are creating an instance on remote computer, call <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a>. When you are creating multiple instances, it is more efficient to obtain a pointer to the class object's <a href="https://msdn.microsoft.com/en-us/library/ms694364(v=VS.85).aspx">IClassFactory</a> interface and use its methods as needed. In the latter case, you should use the <a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a> function.

In the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration, you can specify the type of server used to manage the object. The constants can be CLSCTX_INPROC_SERVER, CLSCTX_INPROC_HANDLER, CLSCTX_LOCAL_SERVER, CLSCTX_REMOTE_SERVER or any combination of these values. The constant CLSCTX_ALL is defined as the combination of all four. For more information about the use of one or a combination of these constants, see <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms682215(v=VS.85).aspx">IClassFactory::CreateInstance</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678507(v=VS.85).aspx">Instance Creation Helper Functions</a>
 

 

