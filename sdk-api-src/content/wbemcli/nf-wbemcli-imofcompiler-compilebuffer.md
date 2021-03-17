---
UID: NF:wbemcli.IMofCompiler.CompileBuffer
title: IMofCompiler::CompileBuffer (wbemcli.h)
description: The IMofCompiler::CompileBuffer method compiles either a buffer containing binary MOF data or a text buffer in ASCII format.
helpviewer_keywords: ["CompileBuffer","CompileBuffer method [Windows Management Instrumentation]","CompileBuffer method [Windows Management Instrumentation]","IMofCompiler interface","IMofCompiler interface [Windows Management Instrumentation]","CompileBuffer method","IMofCompiler.CompileBuffer","IMofCompiler::CompileBuffer","WBEM_FLAG_AUTORECOVER","WBEM_FLAG_CHECK_ONLY","WBEM_FLAG_CONSOLE_PRINT","WBEM_FLAG_DONT_ADD_TO_LIST","_hmm_imofcompiler_compilebuffer","wbemcli/IMofCompiler::CompileBuffer","wmi.imofcompiler_compilebuffer"]
old-location: wmi\imofcompiler_compilebuffer.htm
tech.root: wmi
ms.assetid: 7f3cc061-839e-49c2-a225-452719f155a9
ms.date: 12/05/2018
ms.keywords: CompileBuffer, CompileBuffer method [Windows Management Instrumentation], CompileBuffer method [Windows Management Instrumentation],IMofCompiler interface, IMofCompiler interface [Windows Management Instrumentation],CompileBuffer method, IMofCompiler.CompileBuffer, IMofCompiler::CompileBuffer, WBEM_FLAG_AUTORECOVER, WBEM_FLAG_CHECK_ONLY, WBEM_FLAG_CONSOLE_PRINT, WBEM_FLAG_DONT_ADD_TO_LIST, _hmm_imofcompiler_compilebuffer, wbemcli/IMofCompiler::CompileBuffer, wmi.imofcompiler_compilebuffer
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
 - IMofCompiler::CompileBuffer
 - wbemcli/IMofCompiler::CompileBuffer
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
 - IMofCompiler.CompileBuffer
---

# IMofCompiler::CompileBuffer


## -description

The <b>IMofCompiler::CompileBuffer</b> method compiles either a buffer containing binary MOF data or a text buffer in ASCII format. Binary MOF files contain parsed data and  must be stored in the database. 
The <b>CompileBuffer</b> method only accepts multi-byte character arrays (string buffers) that are not <b>NULL</b>-terminated.

## -parameters

### -param BuffSize [in]

Size of the data pointed to by the <i>pBuffer</i> parameter.

### -param pBuffer [in]

Pointer to the binary MOF file data or a text buffer in ASCII format.

### -param ServerAndNamespace [in]

Name of the server and namespace.

This parameter is ignored unless the <i>pBuffer</i> parameter points to a text buffer.  If the text MOF is passed without a <a href="/windows/desktop/WmiSdk/-pragma">#pragma</a> statement, then the MOF file is compiled into the default namespace. If <i>pBuffer</i> points to a binary MOF file, then the <i>ServerAndNamespace</i> parameter must be <b>NULL</b>.

### -param User [in]

Name of the user requesting the service.

This parameter specifies the credentials for compiling on remote computers. If the value is <b>NULL</b>, then the user context is whatever the current process is using. This is always ignored when connecting to the local computer. For more information, see the Remarks section.

### -param Authority [in]

Specifies the credentials for compiling on remote computers. If the value is <b>NULL</b>, the authority context is whatever the current process is using. This parameter is always ignored when connecting to the local computer. For more information, see the Remarks section.

### -param Password [in]

Specifies the credentials for compiling on remote computers. If the value is <b>NULL</b>, the password of the current context is used. This parameter is always ignored when connecting to the local computer.

### -param lOptionFlags [in]

You can combine one or more of the following flags.



#### WBEM_FLAG_CHECK_ONLY

Performs only a syntax check.



#### WBEM_FLAG_AUTORECOVER

If the method is successful, it adds the file name  to the list of files to be compiled during automatic database recovery.

This flag cannot be combined with  the namespace, class, or instance flags.



#### WBEM_FLAG_CONSOLE_PRINT

Sends various useful messages to the console.



#### WBEM_FLAG_DONT_ADD_TO_LIST

Prevents the addition of the file to the list of files to be compiled during automatic database recovery.

This flag is not compatible with <b>WBEM_FLAG_AUTORECOVER</b>.

### -param lClassFlags [in]

This parameter is ignored because the binary MOF file already contains the information. The parameter value should be 0.

### -param lInstanceFlags [in]

Ignored because the binary MOF file already contains the information. The parameter value should be 0.

### -param pInfo [in, out]

Pointer to a <a href="/windows/win32/api/wbemcli/ns-wbemcli-wbem_compile_status_info">WBEM_COMPILE_STATUS_INFO</a> that describes an error.

If the parameter value is not <b>NULL</b>, an error has occurred, and the structure is filled  with error information.

## -returns

This method returns <b>WBEM_S_NO_ERROR</b> if successful. If the method is unsuccessful, it returns <b>WBEM_S_FALSE</b>.

## -remarks

If the <i>User</i> parameter takes the form &lt;<i>domain\user</i>&gt;, the <i>Authority</i> parameter must be <b>NULL</b>.

Binary MOF data can be generated by the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-imofcompiler-createbmof">CreateBMOF</a> method, which stores the binary MOF data into a file that can be read before calling the 
<b>CompileBuffer</b> method.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-imofcompiler">IMofCompiler</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_compiler_options">WBEM_COMPILER_OPTIONS</a>