---
UID: NN:wbemcli.IMofCompiler
title: IMofCompiler
author: windows-sdk-content
description: The IMofCompiler interface, implemented by Mofd.dll, provides a COM interface that is used by the Managed Object Format (MOF) compiler and any other applications that compile MOF files.
old-location: wmi\imofcompiler.htm
tech.root: WmiSdk
ms.assetid: 5e01c7ac-7090-4cde-b836-01fa9d3f27f5
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IMofCompiler, IMofCompiler interface [Windows Management Instrumentation], IMofCompiler interface [Windows Management Instrumentation],described, MofCompiler, _hmm_imofcompiler, wbemcli/IMofCompiler, wmi.imofcompiler
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: Wbemuuid.lib
req.dll: Mofd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mofd.dll
api_name:
 - IMofCompiler
 - MofCompiler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMofCompiler interface


## -description


The 
<b>IMofCompiler</b> interface, implemented by Mofd.dll, provides a COM interface that is used by the <a href="gloss_m.htm">Managed Object Format</a> (MOF) compiler and any other applications that compile MOF files. Objects defined as classes in the MOF files can be obtained using the <b>CLSID_MofCompiler</b> CLSID value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMofCompiler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMofCompiler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Structures</a></li>
</ul>

## -members

The <b>IMofCompiler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f3cc061-839e-49c2-a225-452719f155a9">CompileBuffer</a>
</td>
<td align="left" width="63%">
Takes the information in a buffer and stores it in Windows Management. The buffer must contain binary MOF data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caf13a5c-2aca-4acb-8210-909737bf1022">CompileFile</a>
</td>
<td align="left" width="63%">
Compiles a particular MOF file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39c5d621-0cdf-44e2-9ec0-c68299e85cb7">CreateBMOF</a>
</td>
<td align="left" width="63%">
Reads a MOF file and outputs binary MOF data to another file.

</td>
</tr>
</table> 
<h3><a id="structs"></a>Structures</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMofCompiler</b> interface has these structures.
<table>
<tr>
<th align="left" width="37%">Structure</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94B3516F-2DDA-4C93-B48E-67D7FE357F4E">WBEM_COMPILE_STATUS_INFO</a>
</td>
<td align="left" width="63%">
Describes an error for the <b>IMofCompiler</b> interface.

</td>
</tr>
</table> 


## -remarks



<b>Windows 8:  </b>When installing a provider the <b>IMofCompiler</b> interface treats the [Key] and [Static] qualifiers as true if they are present, regardless of their actual values. Other qualifiers are treated as false if they are present but not explicitly set to true.


#### Examples

The following code is an example of how to create a pointer to an <b>IMofCompiler</b> object.


```cpp
IMofCompiler *pMof = NULL;
CoCreateInstance(
    CLSID_MofCompiler,
    0,
    CLSCTX_INPROC_SERVER,
    IID_IMofCompiler,
    (LPVOID *) &pMof);
```





## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for
    WMI</a>



<a href="https://msdn.microsoft.com/c09209ea-5283-4779-9481-71a24b03002f">MOF Data Types</a>



<a href="https://msdn.microsoft.com/1760f1bd-7027-4201-97a2-ca902f945b52">Running the MOF Compiler on a File</a>



<a href="https://msdn.microsoft.com/9858da09-fb91-43a4-9817-83b10e2ee08f">mofcomp</a>
 

 

