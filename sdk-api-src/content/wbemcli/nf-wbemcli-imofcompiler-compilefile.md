---
UID: NF:wbemcli.IMofCompiler.CompileFile
title: IMofCompiler::CompileFile (wbemcli.h)
description: The IMofCompiler::CompileFile method compiles a MOF file (including binary MOFs) and stores the information in the WMI repository.
helpviewer_keywords: ["CompileFile","CompileFile method [Windows Management Instrumentation]","CompileFile method [Windows Management Instrumentation]","IMofCompiler interface","IMofCompiler interface [Windows Management Instrumentation]","CompileFile method","IMofCompiler.CompileFile","IMofCompiler::CompileFile","WBEM_FLAG_AUTORECOVER","WBEM_FLAG_CHECK_ONLY","WBEM_FLAG_CONSOLE_PRINT","WBEM_FLAG_CREATE_ONLY","WBEM_FLAG_DONT_ADD_TO_LIST","WBEM_FLAG_UPDATE_FORCE_MODE","WBEM_FLAG_UPDATE_ONLY","WBEM_FLAG_UPDATE_SAFE_MODE","_hmm_imofcompiler_compilefile","wbemcli/IMofCompiler::CompileFile","wmi.imofcompiler_compilefile"]
old-location: wmi\imofcompiler_compilefile.htm
tech.root: wmi
ms.assetid: caf13a5c-2aca-4acb-8210-909737bf1022
ms.date: 12/05/2018
ms.keywords: CompileFile, CompileFile method [Windows Management Instrumentation], CompileFile method [Windows Management Instrumentation],IMofCompiler interface, IMofCompiler interface [Windows Management Instrumentation],CompileFile method, IMofCompiler.CompileFile, IMofCompiler::CompileFile, WBEM_FLAG_AUTORECOVER, WBEM_FLAG_CHECK_ONLY, WBEM_FLAG_CONSOLE_PRINT, WBEM_FLAG_CREATE_ONLY, WBEM_FLAG_DONT_ADD_TO_LIST, WBEM_FLAG_UPDATE_FORCE_MODE, WBEM_FLAG_UPDATE_ONLY, WBEM_FLAG_UPDATE_SAFE_MODE, _hmm_imofcompiler_compilefile, wbemcli/IMofCompiler::CompileFile, wmi.imofcompiler_compilefile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMofCompiler::CompileFile
 - wbemcli/IMofCompiler::CompileFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mofd.dll
api_name:
 - IMofCompiler.CompileFile
---

# IMofCompiler::CompileFile


## -description

The <b>IMofCompiler::CompileFile</b> method compiles a MOF file (including 
    binary MOFs) and stores the information in the 
    <a href="/windows/desktop/WmiSdk/gloss-w">WMI repository</a>. 
    This method performs the same operation as the <a href="/windows/desktop/WmiSdk/mofcomp">Mofcomp</a> 
    command.

## -parameters

### -param FileName [in]

The name of the file to be compiled.

### -param ServerAndNamespace [in]

The path to the default namespace where any classes or instance are written.

You can specify a namespace on a remote computer ("\\computer\root", for 
       example). This value can be overridden by the <b>#pragma</b> command and should not be used if 
       auto recovery is desired. If <b>NULL</b>, then the root\default namespace on the local 
       computer is the default.

### -param User [in]

A value that specifies the credentials used to compile on remote computers. If the value is 
      <b>NULL</b>, the user context is whatever the calling process is using. This is always 
      ignored when connecting to the local computer. For more information, see the Remarks section.

### -param Authority [in]

A value that specifies the credentials for compiling on remote computers. If the value is 
      <b>NULL</b>, the authority context is whatever the calling process is using. This is always 
      ignored when connecting to the local computer. For more information, see the Remarks section.

### -param Password [in]

A value that specifies the credentials for compiling on remote computers. If the value is <b>NULL</b>, the password of the current context is used. This is always ignored when connecting to the local computer.

### -param lOptionFlags [in]

A parameter that, when the 
<b>CompileFile</b> method is used, enables the combination of one or more of the following flags.



#### WBEM_FLAG_CHECK_ONLY

Performs only a syntax check.



#### WBEM_FLAG_AUTORECOVER

If the method is successful, adds the name of the file to the list of files to be compiled during automatic database recovery.

Be aware that this flag cannot be combined with either the namespace, class, or instance flags.



#### WBEM_FLAG_CONSOLE_PRINT

Sends various useful messages to the console.



#### WBEM_FLAG_DONT_ADD_TO_LIST

Prevents the file from being added to the list of files compiled during automatic database recovery.

This flag is not compatible with <b>WBEM_FLAG_AUTORECOVER</b>.

### -param lClassFlags [in]

The flags that control the creation of classes.

Parameters may be 0 or a combination of the following values.



#### WBEM_FLAG_UPDATE_ONLY

Prevents creation of a class.

You can combine this flag with either <b>WBEM_FLAG_UPDATE_SAFE_MODE</b> or <b>WBEM_FLAG_UPDATE_FORCE_MODE</b>.



#### WBEM_FLAG_CREATE_ONLY

Allows only class creation.

You may not combine this flag with the other flags.



#### WBEM_FLAG_UPDATE_SAFE_MODE

Updates the class unless conflicts exist.

You may combine this flag with <b>WBEM_FLAG_UPDATE_ONLY</b>.



#### WBEM_FLAG_UPDATE_FORCE_MODE

Updates and resolves conflicts wherever possible. Using force mode to update a static class results in the deletion of all instances of that class. Force update on a provider class does not delete instances of the class.

You may combine this flag with <i>llnstanceFlags</i>.

### -param lInstanceFlags [in]

The flags that control the creation of instances.

Parameter values can be either 0 or one of the following flags.



#### WBEM_FLAG_UPDATE_ONLY

Only allow updates.



#### WBEM_FLAG_CREATE_ONLY

Allow only new instances.

### -param pInfo [in, out]

Pointer to a <a href="/windows/win32/api/wbemcli/ns-wbemcli-wbem_compile_status_info">WBEM_COMPILE_STATUS_INFO</a> that describes an error.

If the parameter value is not <b>NULL</b>, an error has occurred, and the structure is filled  with error information.

## -returns

This method can return one of these values.

2

Warning that <a href="/windows/desktop/WmiSdk/pragma-autorecover">#pragma autorecover</a> statement is not present. This statement should be one the first line of the MOF file.

## -remarks

If the <i>User</i> parameter is in the form of &lt;<i>domain\user</i>&gt;, the <i>Authority</i> parameter must be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-imofcompiler">IMofCompiler</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_change_flag_type">WBEM_CHANGE_FLAG_TYPE</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_compiler_options">WBEM_COMPILER_OPTIONS</a>



<a href="/windows/desktop/WmiSdk/mofcomp">mofcomp</a>