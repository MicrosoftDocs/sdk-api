---
UID: NF:wbemcli.IWbemClassObject.PutMethod
title: IWbemClassObject::PutMethod
author: windows-sdk-content
description: Used to create a method.
old-location: wmi\iwbemclassobject_putmethod.htm
old-project: WmiSdk
ms.assetid: eebfe049-e30e-40e0-a3bd-85a4bc11582f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],PutMethod method, IWbemClassObject.PutMethod, IWbemClassObject::PutMethod, PutMethod, PutMethod method [Windows Management Instrumentation], PutMethod method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_putmethod, wbemcli/IWbemClassObject::PutMethod, wmi.iwbemclassobject_putmethod
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CIMWin32.dll
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipiprt.dll
api_name:
 - IWbemClassObject.PutMethod
product: Windows
targetos: Windows
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemClassObject::PutMethod


## -description


The  <b>IWbemClassObject::PutMethod</b> is used to create a method. This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointers that point to CIM instances.

The user cannot create methods with names that begin or end with an underscore. This is reserved for system classes and properties.


## -parameters




### -param wszName [in]

The method name that is  created.


### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param pInSignature [in]

A pointer to a copy of the <a href="https://msdn.microsoft.com/d973feb5-27c4-4d8e-bf1b-0a455afa4375">__Parameters</a> system class that contains the in parameters for the method. This parameter is ignored if set to <b>NULL</b>.


### -param pOutSignature [in]

A pointer to a copy of the <a href="https://msdn.microsoft.com/d973feb5-27c4-4d8e-bf1b-0a455afa4375">__Parameters</a> system class that contains the out parameters for the object. This parameter is ignored if set to <b>NULL</b>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



For a method, the in and out parameters are described as properties in 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> objects.

For example, consider the following method:

<div class="code"><span codelanguage="mof"><table>
<tr>
<th>mof</th>
</tr>
<tr>
<td>
<pre>Class MyClass{
    [key] string KeyVal;
    sint32 PropVal;
    sint32 ExampleMethod([in] sint32 Param1, [in] uint32 Param2, 
        [out] string Param3);
    HRESULT ReturnValue;
};</pre>
</td>
</tr>
</table></span></div>
In the previous example, the class has one method. To create the method programmatically, the user calls 
<b>IWbemClassObject::PutMethod</b> with the <i>pInSignature</i> parameter that points to a copy of the system class 
<a href="https://msdn.microsoft.com/d973feb5-27c4-4d8e-bf1b-0a455afa4375">__Parameters</a> that contains two properties: <b>Param1</b> and <b>Param2</b>. The <i>pOutSignature</i> points to a copy of the system class <b>__Parameters</b>  that contains two properties: <b>Param3</b> and <b>ReturnValue</b>.

The <b>ReturnValue</b> property of the object pointed to by <i>pOutSignature</i> determines the method return type. If <i>pOutSignature</i> is set to <b>NULL</b>, the return type is assumed to be VOID.

An [in/out] parameter can be defined by adding the same property to both objects pointed to by the <i>pInSignature</i> and <i>pOutSignature</i> parameters.  In this case, the properties share the same <b>ID</b> qualifier value.

Each property in a <a href="https://msdn.microsoft.com/d973feb5-27c4-4d8e-bf1b-0a455afa4375">__Parameters</a> class object other than <b>ReturnValue</b> must have an <b>ID</b> qualifier, a zero-based numeric that identifies the order in which the parameters appear. In this example, <b>Param1</b> would be 0, <b>Param2</b> 1, and <b>Param3</b> 2. No two parameters can have the same <b>ID</b> value, and no <b>ID</b> value can be skipped. If either condition occurs, 
<b>IWbemClassObject::PutMethod</b> returns <b>WBEM_E_NONCONSECUTIVE_PARAMETER_IDS</b>.

<div class="alert"><b>Note</b>  The caller must call <b>IWbemClassObject::Release</b> on the <i>pInSignature</i> and <i>pOutSignature</i> pointers when these objects are no longer required.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/71cbecde-33c4-4bf1-9793-bef6d823dcac">Creating a Method</a>



<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/d4775fe0-62bf-40a6-8e2c-7bc8c3d92e1f">IWbemClassObject::GetMethod</a>
 

 

