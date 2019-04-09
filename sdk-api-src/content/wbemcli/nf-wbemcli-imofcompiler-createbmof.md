---
UID: NF:wbemcli.IMofCompiler.CreateBMOF
title: IMofCompiler::CreateBMOF (wbemcli.h)
author: windows-sdk-content
description: The IMofCompiler::CreateBMOF method creates a binary MOF file.
old-location: wmi\imofcompiler_createbmof.htm
tech.root: WmiSdk
ms.assetid: 39c5d621-0cdf-44e2-9ec0-c68299e85cb7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBMOF, CreateBMOF method [Windows Management Instrumentation], CreateBMOF method [Windows Management Instrumentation],IMofCompiler interface, IMofCompiler interface [Windows Management Instrumentation],CreateBMOF method, IMofCompiler.CreateBMOF, IMofCompiler::CreateBMOF, WBEM_FLAG_CHECK_ONLY, WBEM_FLAG_CREATE_ONLY, WBEM_FLAG_UPDATE_FORCE_MODE, WBEM_FLAG_UPDATE_ONLY, WBEM_FLAG_UPDATE_SAFE_MODE, WBEM_FLAG_WMI_CHECK, WBEM_FLAT_CONSOLE_PRINT, _hmm_imofcompiler_createbmof, wbemcli/IMofCompiler::CreateBMOF, wmi.imofcompiler_createbmof
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
 - IMofCompiler.CreateBMOF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMofCompiler::CreateBMOF


## -description


The <b>IMofCompiler::CreateBMOF</b> method creates a binary MOF file. File creation is accomplished by parsing a regular MOF file and storing a binary representation of the classes and instances into a special file format. Typically, this data binary large object (BLOB) is stored as a resource in an executable file, which can later be extracted for a call to the 
<a href="https://msdn.microsoft.com/7f3cc061-839e-49c2-a225-452719f155a9">CompileBuffer</a> method. The <b>IMofCompiler::CreateBMOF</b> can also be used to create a localized MOF file (.mfl).


## -parameters




### -param TextFileName [in]

The name of the text file to be parsed.


### -param BMOFFileName [in]

<b>Binary MOF file:  </b>The name of the file in which the resulting binary MOF data is to be stored.

<b>Localized MOF file:  </b>The <i>BMOFFileName</i> string must contain the following comma-separated values:

<ul>
<li>
a&lt;locale&gt;

Specifies the locale information. This value must start with a preceding comma. For more information, see the description of the <b>-ADMENDMENT</b> switch for the <a href="https://msdn.microsoft.com/9858da09-fb91-43a4-9817-83b10e2ee08f">mofcomp</a> utility.

</li>
<li>
n&lt;filename.mof&gt;

The name of the file in which the resulting binary MOF data is to be stored.

</li>
<li>
l&lt;filename.mfl&gt;

The name of the file in which the resulting localized MOF data is to be stored.

</li>
</ul>
For example,  <i>BMOFFileName</i>=",aMS_409,nmyFile.mof,lmyFile.mfl".




### -param ServerAndNamespace [in]

The path of the default namespace, where classes or instances are written.

You can use this parameter to specify a namespace on a remote computer ("\\computer\root", for example). This value may be overridden by the 
<a href="https://msdn.microsoft.com/3cf22686-dd56-43a3-9584-3d707a20a3a0">#pragma</a> command and should not be used if you use autorecovery. If the parameter value is <b>NULL</b>, the root\default namespace on the local computer is the default.


### -param lOptionFlags [in]

You can combine one or more of the following flags.



#### WBEM_FLAG_CHECK_ONLY

Performs only a syntax check.



#### WBEM_FLAT_CONSOLE_PRINT

Sends various useful messages to the console.



#### WBEM_FLAG_WMI_CHECK

Performs additional checks on the resulting binary MOF file using the WMIMOFCHK program, which is part of the WMI section of the Windows SDK.


### -param lClassFlags [in]

The flags that control the creation of classes. The parameter value may be 0 or a combination of the following flags.



#### WBEM_FLAG_UPDATE_ONLY

Prevents class creation.

You can combine this flag with either <b>WBEM_FLAG_UPDATE_SAFE_MODE</b> or <b>WBEM_FLAG_UPDATE_FORCE_MODE</b>.



#### WBEM_FLAG_CREATE_ONLY

Permits only class creation.

You cannot combine this with other flags.



#### WBEM_FLAG_UPDATE_SAFE_MODE

Updates the class unless conflicts exist.

You can combine this flag with <b>WBEM_FLAG_UPDATE_ONLY</b>.



#### WBEM_FLAG_UPDATE_FORCE_MODE

Updates and resolves conflicts when possible. Using force mode to update a static class results in the deletion of all instances of that class. Forces an update for a provider class does not delete instances of the class.

You can combine this flag with <i>lInstanceFlags</i>.


### -param lInstanceFlags [in]

Flags controlling the creation of instances.

The parameter value may be either 0 or one of the following flags.



#### WBEM_FLAG_UPDATE_ONLY

Permits only updates.



#### WBEM_FLAG_CREATE_ONLY

Permits only new instances.


### -param pInfo [in, out]

Pointer to a <a href="https://msdn.microsoft.com/94B3516F-2DDA-4C93-B48E-67D7FE357F4E">WBEM_COMPILE_STATUS_INFO</a> that describes an error.

If the parameter value is not <b>NULL</b>, an error has occurred, and the structure is filled  with error information.


## -returns



This method returns <b>WBEM_S_NO_ERROR</b> if successful. If the method is unsuccessful, it returns <b>WBEM_S_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/5e01c7ac-7090-4cde-b836-01fa9d3f27f5">IMofCompiler</a>



<a href="https://msdn.microsoft.com/B36B7D62-13C9-401F-A6C0-7C498A139AEC">WBEM_CHANGE_FLAG_TYPE</a>



<a href="https://msdn.microsoft.com/49F1518B-A487-458F-BFDD-BCF75A0E4306">WBEM_COMPILER_OPTIONS</a>



<a href="https://msdn.microsoft.com/9858da09-fb91-43a4-9817-83b10e2ee08f">mofcomp</a>
 

 

