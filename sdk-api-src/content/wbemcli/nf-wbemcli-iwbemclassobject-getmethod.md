---
UID: NF:wbemcli.IWbemClassObject.GetMethod
title: IWbemClassObject::GetMethod
author: windows-sdk-content
description: Returns information about the requested method.
old-location: wmi\iwbemclassobject_getmethod.htm
tech.root: WmiSdk
ms.assetid: d4775fe0-62bf-40a6-8e2c-7bc8c3d92e1f
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetMethod, GetMethod method [Windows Management Instrumentation], GetMethod method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetMethod method, IWbemClassObject.GetMethod, IWbemClassObject::GetMethod, _hmm_iwbemclassobject_getmethod, wbemcli/IWbemClassObject::GetMethod, wmi.iwbemclassobject_getmethod
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
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
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
 - IWbemClassObject.GetMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemClassObject::GetMethod


## -description


The 
<b>IWbemClassObject::GetMethod</b> method returns information about the requested method. This call is only supported if the current object is a CIM class definition. Method information is not available from 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointers which point to CIM instances.


## -parameters




### -param wszName [in]

The method name. This cannot be <b>NULL</b>, and must point to a valid <b>LPCWSTR</b>.


### -param lFlags [in]

Reserved. This parameter must be 0.


### -param ppInSignature [out]

A pointer that receives an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointer which describes the in parameters to the method. This parameter is  ignored if set to <b>NULL</b>. Be aware that Windows Management can set the 
<b>IWbemClassObject</b> pointer to <b>NULL</b> if this method has no in parameters. For more information, see Remarks.


### -param ppOutSignature [out]

A pointer that receives an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointer which describes the out-parameters to the method. This parameter will be ignored if set to <b>NULL</b>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



For a method, the in and out parameters are described as properties in an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>, an instance of the system class 
<a href="https://msdn.microsoft.com/d973feb5-27c4-4d8e-bf1b-0a455afa4375">__Parameters</a>.

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
    sint32 ExampleMethod([in] sint32 Parm1, [in] uint32 Parm2, 
      [out] string Parm3);
};</pre>
</td>
</tr>
</table></span></div>
In this example, the class has a single method. When the user calls 
<b>IWbemClassObject::GetMethod</b>, the <i>ppInSignature</i> parameter receives an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object, which contains two properties: <b>Parm1</b> and <b>Parm2</b>. The <i>ppOutSignature</i> parameter contains two properties, <b>Parm3</b> and <b>ReturnValue</b>.

After filling in the property values of the <i>ppInSignature</i> object, the caller can use the object to execute the method by calling 
<a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a> or 
<a href="https://msdn.microsoft.com/61966c03-80dc-4556-b2fc-97e879cf458c">IWbemServices::ExecMethodAsync</a>.

<div class="alert"><b>Note</b>  The caller must call <b>IWbemClassObject::Release</b> on the <i>ppInSignature</i> and <i>ppOutSignature</i> pointers when these objects are no longer required.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/eebfe049-e30e-40e0-a3bd-85a4bc11582f">IWbemClassObject::PutMethod</a>
 

 

