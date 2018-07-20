---
UID: NF:combaseapi.DllGetClassObject
title: DllGetClassObject function
author: windows-sdk-content
description: Retrieves the class object from a DLL object handler or object application.
old-location: com\dllgetclassobject.htm
old-project: com
ms.assetid: 42c08149-c251-47f7-a81f-383975d7081c
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DllGetClassObject, DllGetClassObject function [COM], _com_DllGetClassObject, com.dllgetclassobject, combaseapi/DllGetClassObject
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - combaseapi.h
api_name:
 - DllGetClassObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DllGetClassObject function


## -description


Retrieves the class object from a DLL object handler or object application.

OLE does not provide this function. DLLs that support the OLE Component Object Model (COM) must implement <b>DllGetClassObject</b> in OLE object handlers or DLL applications.


## -parameters




### -param rclsid [in]

The CLSID that will associate the correct data and code.


### -param riid [in]

A reference to the identifier of the interface that the caller is to use to communicate with the class object. Usually, this is IID_IClassFactory (defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a>).


### -param ppv [out]

The address of a pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppv</i> contains the requested interface pointer. If an error occurs, the interface pointer is <b>NULL</b>.



## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The object was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLASS_E_CLASSNOTAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The DLL does not support the class (object definition).

</td>
</tr>
</table>
 




## -remarks



If a call to the <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> function finds the class object that is to be loaded in a DLL, <b>CoGetClassObject</b> uses the DLL's exported <b>DllGetClassObject</b> function. 



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You should not call <b>DllGetClassObject</b> directly. When an object is defined in a DLL, <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> calls the <a href="https://msdn.microsoft.com/be0d9e82-2438-488e-88c3-68dc7ac3e16f">CoLoadLibrary</a> function to load the DLL, which, in turn, calls <b>DllGetClassObject</b>. 



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You need to implement <b>DllGetClassObject</b> in (and export it from) DLLs that support COM.



#### Examples

The following is an example (in C++) of an implementation of <b>DllGetClassObject</b>. In this example, <b>DllGetClassObject</b> creates a class object and calls its <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method to retrieve a pointer to the interface requested in riid. The implementation releases the reference it holds to the <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a> interface because it returns a reference-counted pointer to <b>IClassFactory</b> to the caller.



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT_export CALLBACK DllGetClassObject 
    (REFCLSID rclsid, REFIID riid, LPVOID * ppvObj) 
{ 
    HRESULT hr = E_OUTOFMEMORY; 
    *ppvObj = NULL; 
 
    CClassFactory *pClassFactory = new CClassFactory(rclsid); 
    if (pClassFactory != NULL)   { 
        hr = pClassFactory-&gt;QueryInterface(riid, ppvObj); 
        pClassFactory-&gt;Release(); 
    } 
    return hr;
} 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/a47df9eb-97cb-4875-a121-1dabe7bc9db6">DllCanUnloadNow</a>
 

 

