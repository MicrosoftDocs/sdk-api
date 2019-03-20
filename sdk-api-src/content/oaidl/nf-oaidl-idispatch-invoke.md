---
UID: NF:oaidl.IDispatch.Invoke
title: IDispatch::Invoke (oaidl.h)
author: windows-sdk-content
description: Provides access to properties and methods exposed by an object.
old-location: automat\idispatch_invoke.htm
tech.root: automat
ms.assetid: 964ade8e-9d8a-4d32-bd47-aa678912a54d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DISPATCH_METHOD, DISPATCH_PROPERTYGET, DISPATCH_PROPERTYPUT, DISPATCH_PROPERTYPUTREF, IDispatch interface [Automation],Invoke method, IDispatch.Invoke, IDispatch::Invoke, Invoke, Invoke method [Automation], Invoke method [Automation],IDispatch interface, _oa96_IDispatch::Invoke, automat.idispatch_invoke, oaidl/IDispatch::Invoke
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IDispatch.Invoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDispatch::Invoke


## -description


Provides access to properties and methods exposed by an object. The dispatch function <a href="https://msdn.microsoft.com/69b89e5c-2a04-4a6a-beb0-18e68f8866ac">DispInvoke</a> provides a standard implementation of <b>Invoke</b>.




## -parameters




### -param dispIdMember [in]

Identifies the member. Use <a href="https://msdn.microsoft.com/6f6cf233-3481-436e-8d6a-51f93bf91619">GetIDsOfNames</a> or the object's documentation to obtain the dispatch identifier.


### -param riid [in]

Reserved for future use. Must be IID_NULL.


### -param lcid [in]

The locale context in which to interpret arguments. The <i>lcid</i> is used by the <a href="https://msdn.microsoft.com/6f6cf233-3481-436e-8d6a-51f93bf91619">GetIDsOfNames</a> function, and is also passed to <b>Invoke</b> to allow the object to interpret its arguments specific to a locale.

Applications that do not support multiple national languages can ignore this parameter. For more information, refer to <a href="https://msdn.microsoft.com/47dc5add-232c-4268-b977-43e12da81ede">Supporting Multiple National Languages</a> and <a href="https://msdn.microsoft.com/f488675d-4104-40e9-8ee1-265ce92188b3">Exposing ActiveX Objects</a>.


### -param wFlags [in]

Flags describing the context of the <b>Invoke</b> call.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_METHOD"></a><a id="dispatch_method"></a><dl>
<dt><b>DISPATCH_METHOD</b></dt>
</dl>
</td>
<td width="60%">
The member is invoked as a method. If a property has the same name, both this and the DISPATCH_PROPERTYGET flag can be set.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYGET"></a><a id="dispatch_propertyget"></a><dl>
<dt><b>DISPATCH_PROPERTYGET</b></dt>
</dl>
</td>
<td width="60%">
The member is retrieved as a property or data member.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYPUT"></a><a id="dispatch_propertyput"></a><dl>
<dt><b>DISPATCH_PROPERTYPUT</b></dt>
</dl>
</td>
<td width="60%">
The member is changed as a property or data member.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYPUTREF"></a><a id="dispatch_propertyputref"></a><dl>
<dt><b>DISPATCH_PROPERTYPUTREF</b></dt>
</dl>
</td>
<td width="60%">
The member is changed by a reference assignment, rather than a value assignment. This flag is valid only when the property accepts a reference to an object.


</td>
</tr>
</table>
 


### -param pDispParams [in, out]

Pointer to a DISPPARAMS structure containing an array of arguments, an array of argument DISPIDs for named arguments, and counts for the number of elements in the arrays.


### -param pVarResult [out]

Pointer to the location where the result is to be stored, or NULL if the caller expects no result. This argument is ignored if DISPATCH_PROPERTYPUT or DISPATCH_PROPERTYPUTREF is specified.


### -param pExcepInfo [out]

Pointer to a structure that contains exception information. This structure should be filled in if DISP_E_EXCEPTION is returned. Can be NULL.


### -param puArgErr [out]

The index within rgvarg of the first argument that has an error. Arguments are stored in pDispParams-&gt;rgvarg in reverse order, so the first argument is the one with the highest index in the array. This parameter is returned only when the resulting return value is DISP_E_TYPEMISMATCH or DISP_E_PARAMNOTFOUND. This argument can be set to null. For details, see <a href="https://msdn.microsoft.com/8eaff01a-f038-4fca-8951-7d0efcfdf1e1">Returning Errors</a>.



## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADPARAMCOUNT</b></dt>
</dl>
</td>
<td width="60%">
The number of elements provided to DISPPARAMS is different from the number of arguments accepted by the method or property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments in DISPPARAMS is not a valid variant type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
The application needs to raise an exception. In this case, the structure passed in <i>pexcepinfo</i> should be filled in.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested member does not exist.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_NONAMEDARGS</b></dt>
</dl>
</td>
<td width="60%">
This implementation of <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> does not support named arguments.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments in DISPPARAMS could not be coerced to the specified type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_PARAMNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter IDs does not correspond to a parameter on the method. In this case, <i>puArgErr</i> is set to the first argument that contains the error.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments could not be coerced. The index of the first parameter with the incorrect type within rgvarg is returned in <i>puArgErr</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_UNKNOWNINTERFACE

</b></dt>
</dl>
</td>
<td width="60%">
The interface identifier passed in riid is not IID_NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_UNKNOWNLCID
</b></dt>
</dl>
</td>
<td width="60%">
The member being invoked interprets string arguments according to the LCID, and the LCID is not recognized. If the LCID is not needed to interpret arguments, this error should not be returned

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_PARAMNOTOPTIONAL</b></dt>
</dl>
</td>
<td width="60%">
A required parameter was omitted.

</td>
</tr>
</table>
 




## -remarks



Generally, you should not implement <b>Invoke</b> directly. Instead, use the dispatch interface to create functions <a href="https://msdn.microsoft.com/45a59243-df93-41ca-ac60-354cb1165004">CreateStdDispatch</a> and <a href="https://msdn.microsoft.com/69b89e5c-2a04-4a6a-beb0-18e68f8866ac">DispInvoke</a>. For details, refer to <b>CreateStdDispatch</b>, <b>DispInvoke</b>, <a href="https://msdn.microsoft.com/0606fe11-59e3-4ce1-bde1-a34cfbf0b093">Creating the IDispatch Interface</a> and <a href="https://msdn.microsoft.com/f488675d-4104-40e9-8ee1-265ce92188b3">Exposing ActiveX Objects</a>. 

If some application-specific processing needs to be performed before calling a member, the code should perform the necessary actions, and then call <a href="https://msdn.microsoft.com/en-us/library/ms221652(v=VS.85).aspx">ITypeInfo::Invoke</a> to invoke the member. <b>ITypeInfo::Invoke</b> acts exactly like <b>Invoke</b>. The standard implementations of <b>Invoke</b> created by <b>CreateStdDispatch</b> and <b>DispInvoke</b> defer to <b>ITypeInfo::Invoke</b>.

In an ActiveX client, <b>Invoke</b> should be used to get and set the values of properties, or to call a method of an ActiveX object. The <i>dispIdMember</i> argument identifies the member to invoke. The DISPIDs that identify members are defined by the implementor of the object and can be determined by using the object's documentation, the <a href="https://msdn.microsoft.com/en-us/library/ms221306(v=VS.85).aspx">IDispatch::GetIDsOfNames</a> function, or the <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> interface.

When you use <b>IDispatch::Invoke()</b> with DISPATCH_PROPERTYPUT or DISPATCH_PROPERTYPUTREF, you have to specially initialize the <b>cNamedArgs</b> and <b>rgdispidNamedArgs</b> elements of your DISPPARAMS structure with the following: 


```cpp
DISPID dispidNamed = DISPID_PROPERTYPUT;
dispparams.cNamedArgs = 1;
dispparams.rgdispidNamedArgs = &dispidNamed;
```


The information that follows addresses developers of ActiveX clients and others who use code to expose ActiveX objects. It describes the behavior that users of exposed objects should expect.




## -see-also




<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

