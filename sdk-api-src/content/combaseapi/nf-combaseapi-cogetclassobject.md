---
UID: NF:combaseapi.CoGetClassObject
title: CoGetClassObject function (combaseapi.h)
description: Provides a pointer to an interface on a class object associated with a specified CLSID.
helpviewer_keywords: ["CoGetClassObject","CoGetClassObject function [COM]","_com_CoGetClassObject","com.cogetclassobject","combaseapi/CoGetClassObject"]
old-location: com\cogetclassobject.htm
tech.root: com
ms.assetid: 65e758ce-50a4-49e8-b3b2-0cd148d2781a
ms.date: 12/05/2018
ms.keywords: CoGetClassObject, CoGetClassObject function [COM], _com_CoGetClassObject, com.cogetclassobject, combaseapi/CoGetClassObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoGetClassObject
 - combaseapi/CoGetClassObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetClassObject
---

# CoGetClassObject function


## -description

 Provides a pointer to an interface on a class object associated with a specified CLSID. <b>CoGetClassObject</b> locates, and if necessary, dynamically loads the executable code required to do this.


Call <b>CoGetClassObject</b> directly to create multiple objects through a class object for which there is a CLSID in the system registry. You can also retrieve a class object from a specific remote computer. Most class objects implement the <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> interface. You would then call <a href="/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">CreateInstance</a> to create an uninitialized object. It is not always necessary to go through this process however. To create a single object, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function, which allows you to create an instance on a remote machine. This replaces the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function, which can still be used to create an instance on a local computer. Both functions encapsulate connecting to the class object, creating the instance, and releasing the class object. Two other functions, <a href="/windows/desktop/api/objbase/nf-objbase-cogetinstancefromfile">CoGetInstanceFromFile</a> and <a href="/windows/desktop/api/objbase/nf-objbase-cogetinstancefromistorage">CoGetInstanceFromIStorage</a>, provide both instance creation on a remote system and object activation. There are numerous functions and interface methods whose purpose is to create objects of a single type and provide a pointer to an interface on that object.

## -parameters

### -param rclsid [in]

The CLSID associated with the data and code that you will use to create the objects.

### -param dwClsContext [in]

The context in which the executable code is to be run. To enable a remote activation, include CLSCTX_REMOTE_SERVER. For more information on the context values and their use, see the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> enumeration.

### -param pvReserved [in, optional]

A pointer to computer on which to instantiate the class object. If this parameter is <b>NULL</b>, the class object is instantiated on the current computer or at the computer specified under the class's <a href="/windows/desktop/com/remoteservername">RemoteServerName</a> key, according to the interpretation of the <i>dwClsCtx</i> parameter. See <a href="/windows/desktop/api/objidl/ns-objidl-coserverinfo">COSERVERINFO</a>.

### -param riid [in]

Reference to the identifier of the interface, which will be supplied in _ppv_ on successful return. This interface will be used to communicate with the class object. Typically this value is IID_IClassFactory, although other values such as IID_IClassFactory2 which supports a form of licensing are allowed. All OLE-defined interface IIDs are defined in the OLE header files as IID_interfacename, where interfacename is the name of the interface.

### -param ppv [out]

The address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppv</i> contains the requested interface pointer.

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
Location and connection to the specified class object was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The CLSID is not properly registered. This error can also indicate that the value you specified in <i>dwClsContext</i> is not in the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE
</b></dt>
</dl>
</td>
<td width="60%">
Either the object pointed to by <i>ppv</i> does not support the interface identified by <i>riid</i>, or the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> operation on the class object returned E_NOINTERFACE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
There was an error reading the registration database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_DLLNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Either the in-process DLL or handler DLL was not found (depending  on the context).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_APPNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The executable (.exe) was not found (CLSCTX_LOCAL_SERVER only).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
There was a general access failure on load.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ERRORINDLL</b></dt>
</dl>
</td>
<td width="60%">
There is an error in the executable image.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_APPDIDNTREG</b></dt>
</dl>
</td>
<td width="60%">
The executable was launched, but it did not register the class object (and it may have shut down).


</td>
</tr>
</table>

## -remarks

A class object in OLE is an intermediate object that supports an interface that permits operations common to a group of objects. The objects in this group are instances derived from the same object definition represented by a single CLSID. Usually, the interface implemented on a class object is <a href="/windows/desktop/com/implementing-iclassfactory">IClassFactory</a>, through which you can create object instances of a given definition (class).



A call to <b>CoGetClassObject</b> creates, initializes, and gives the caller access (through a pointer to an interface specified with the <i>riid</i> parameter) to the class object. The class object is the one associated with the CLSID that you specify in the <i>rclsid</i> parameter. The details of how the system locates the associated code and data within a computer are transparent to the caller, as is the dynamic loading of any code that is not already loaded. 



If the class context is CLSCTX_REMOTE_SERVER, indicating remote activation is required, the <a href="/windows/desktop/api/objidl/ns-objidl-coserverinfo">COSERVERINFO</a> structure provided in the <i>pServerInfo</i> parameter allows you to specify the computer on which the server is located. For information on the algorithm used to locate a remote server when <i>pServerInfo</i> is <b>NULL</b>, refer to the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> enumeration.



There are two places to find a CLSID for a class:

<ul>
<li>The registry holds an association between CLSIDs and file suffixes, and between CLSIDs and file signatures for determining the class of an object.</li>
<li>When an object is saved to persistent storage, its CLSID is stored with its data.</li>
</ul>
To create and initialize embedded or linked OLE document objects, it is not necessary to call <b>CoGetClassObject</b> directly. Instead, call the <a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a> or <b>OleCreate</b><i>XXX</i> function. These functions encapsulate the entire object instantiation and initialization process, and call, among other functions, <b>CoGetClassObject</b>.



The <i>riid</i> parameter specifies the interface the client will use to communicate with the class object. In most cases, this interface is <a href="/windows/desktop/com/implementing-iclassfactory">IClassFactory</a>. This provides access to the <a href="/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">CreateInstance</a> method, through which the caller can then create an uninitialized object of the kind specified in its implementation. All classes registered in the system with a CLSID must implement <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>. 



In rare cases, however, you may want to specify some other interface that defines operations common to a set of objects. For example, in the way OLE implements monikers, the interface on the class object is <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a>, used to transform the display name of an object into a moniker.



The <i>dwClsContext</i> parameter specifies the execution context, allowing one CLSID to be associated with different pieces of code in different execution contexts. The <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> enumeration specifies the available context flags. <b>CoGetClassObject</b> consults (as appropriate for the context indicated) both the registry and the class objects that are currently registered by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a> function. 



To release a class object, use the class object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method. The function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> is to be used only to remove a class object's CLSID from the system registry.

## -see-also

<a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a>



<a href="/windows/desktop/api/objidl/ns-objidl-coserverinfo">COSERVERINFO</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a>



<a href="/windows/desktop/com/creating-an-object-through-a-class-object">Creating an Object Through a Class Object</a>



<a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>