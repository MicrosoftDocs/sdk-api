---
UID: NS:winbase.tagACTCTXW
title: ACTCTXW (winbase.h)
description: The ACTCTX structure is used by the CreateActCtx function to create the activation context. (Unicode)
helpviewer_keywords: ["*PACTCTXW","ACTCTX","ACTCTX structure [Side-by-side Assemblies]","ACTCTXW","ACTCTX_FLAG_APPLICATION_NAME_VALID","ACTCTX_FLAG_ASSEMBLY_DIRECTORY_VALID","ACTCTX_FLAG_HMODULE_VALID","ACTCTX_FLAG_LANGID_VALID","ACTCTX_FLAG_PROCESSOR_ARCHITECTURE_VALID","ACTCTX_FLAG_RESOURCE_NAME_VALID","ACTCTX_FLAG_SET_PROCESS_DEFAULT","PACTCTX","PACTCTX structure pointer [Side-by-side Assemblies]","_win32_actctx_str","setup.actctx_str","tagACTCTXA","tagACTCTXW","winbase/ACTCTX","winbase/ACTCTXW","winbase/PACTCTX"]
old-location: setup\actctx_str.htm
tech.root: setup
ms.assetid: b6f97f25-1834-44f7-86b7-33339481ba60
ms.date: 12/05/2018
ms.keywords: '*PACTCTXW, ACTCTX, ACTCTX structure [Side-by-side Assemblies], ACTCTXW, ACTCTX_FLAG_APPLICATION_NAME_VALID, ACTCTX_FLAG_ASSEMBLY_DIRECTORY_VALID, ACTCTX_FLAG_HMODULE_VALID, ACTCTX_FLAG_LANGID_VALID, ACTCTX_FLAG_PROCESSOR_ARCHITECTURE_VALID, ACTCTX_FLAG_RESOURCE_NAME_VALID, ACTCTX_FLAG_SET_PROCESS_DEFAULT, PACTCTX, PACTCTX structure pointer [Side-by-side Assemblies], _win32_actctx_str, setup.actctx_str, tagACTCTXA, tagACTCTXW, winbase/ACTCTX, winbase/ACTCTXW, winbase/PACTCTX'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ACTCTXW (Unicode) and ACTCTXW (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACTCTXW, *PACTCTXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagACTCTXW
 - winbase/tagACTCTXW
 - PACTCTXW
 - winbase/PACTCTXW
 - ACTCTXW
 - winbase/ACTCTXW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - ACTCTX
 - ACTCTXW
 - ACTCTXW
---

# ACTCTXW structure


## -description

The 
<b>ACTCTX</b> structure is used by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createactctxa">CreateActCtx</a> function to create the activation context.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure. This is used to determine the version of this structure.

### -field dwFlags

Flags that indicate how the values included in this structure are to be used. Set any undefined bits in <b>dwFlags</b> to 0. If any undefined bits are not set to 0, the call to 
<a href="/windows/desktop/api/winbase/nf-winbase-createactctxa">CreateActCtx</a> that creates the activation context fails and returns an invalid parameter error code. 



<table>
<tr>
<th>Bit flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACTCTX_FLAG_PROCESSOR_ARCHITECTURE_VALID"></a><a id="actctx_flag_processor_architecture_valid"></a><dl>
<dt><b>ACTCTX_FLAG_PROCESSOR_ARCHITECTURE_VALID</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
0x001

</td>
</tr>
<tr>
<td width="40%"><a id="ACTCTX_FLAG_LANGID_VALID"></a><a id="actctx_flag_langid_valid"></a><dl>
<dt><b>ACTCTX_FLAG_LANGID_VALID</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
0x002

</td>
</tr>
<tr>
<td width="40%"><a id="ACTCTX_FLAG_ASSEMBLY_DIRECTORY_VALID"></a><a id="actctx_flag_assembly_directory_valid"></a><dl>
<dt><b>ACTCTX_FLAG_ASSEMBLY_DIRECTORY_VALID</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
0x004

</td>
</tr>
<tr>
<td width="40%"><a id="ACTCTX_FLAG_RESOURCE_NAME_VALID"></a><a id="actctx_flag_resource_name_valid"></a><dl>
<dt><b>ACTCTX_FLAG_RESOURCE_NAME_VALID</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
0x008

</td>
</tr>
<tr>
<td width="40%"><a id="ACTCTX_FLAG_SET_PROCESS_DEFAULT"></a><a id="actctx_flag_set_process_default"></a><dl>
<dt><b>ACTCTX_FLAG_SET_PROCESS_DEFAULT</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
0x010

</td>
</tr>
<tr>
<td width="40%"><a id="ACTCTX_FLAG_APPLICATION_NAME_VALID"></a><a id="actctx_flag_application_name_valid"></a><dl>
<dt><b>ACTCTX_FLAG_APPLICATION_NAME_VALID</b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
0x020

</td>
</tr>
<tr>
<td width="40%"><a id="ACTCTX_FLAG_HMODULE_VALID"></a><a id="actctx_flag_hmodule_valid"></a><dl>
<dt><b>ACTCTX_FLAG_HMODULE_VALID</b></dt>
<dt>128</dt>
</dl>
</td>
<td width="60%">
0x080

</td>
</tr>
</table>

### -field lpSource

Null-terminated string specifying the path of the manifest file or PE image to be used to create the activation context. If this path refers to an EXE or DLL file, the  <b>lpResourceName</b> member is required.

### -field wProcessorArchitecture

Identifies the type of processor used. Specifies the system's processor architecture.

This value can be one of the following values:

### -field wLangId

Specifies the language manifest that should be used. The default is the current user's current UI language. 

If the requested language cannot be found, an approximation is searched for using the following order: 




<ul>
<li>The current user's specific language. For example, for US English (1033).</li>
<li>The current user's primary language. For example, for English (9).</li>
<li>The current system's specific language.</li>
<li>The current system's primary language.</li>
<li>A nonspecific worldwide language. Language neutral (0).</li>
</ul>

### -field lpAssemblyDirectory

The base directory in which to perform private assembly probing if assemblies in the activation context are not present in the system-wide store.

### -field lpResourceName

Pointer to a null-terminated string that contains the resource name to be loaded from the PE specified in <b>hModule</b> or <b>lpSource</b>. If the resource name is an integer, set this member using MAKEINTRESOURCE. This member is required if   <b>lpSource</b> refers to an EXE or DLL.

### -field lpApplicationName

The name of the current application. If the value of this member is set to null, the name of the executable that launched the current process is used.

### -field hModule

Use this member rather than <b>lpSource</b> if you have already loaded a DLL and wish to use it to create activation contexts rather than using a path in <b>lpSource</b>. See <b>lpResourceName</b> for the rules of looking up resources in this module.

## -remarks

If the file identified by the value of the <b>lpSource</b> member is a PE image file, 
<a href="/windows/desktop/api/winbase/nf-winbase-createactctxa">CreateActCtx</a> searches for the manifest in the .manifest file located in the same directory and in the first RT_MANIFEST resource located in the PE image file. To find a specific named resource from the image, set the <b>lpResourceName</b> to the name of the resource, and add the ACTCTX_FLAG_RESOURCE_NAME_VALID to the <b>dwFlags</b> member. Refer to 
<a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a> for more information on specifying resource names.

In most cases, the caller should not set the ACTCTX_FLAG_PROCESSOR_ARCHITECTURE_VALID and ACTCTX_FLAG_LANGID_VALID flags of the <b>dwFlags</b> member. Also, in most cases, the value of the <b>lpResourceName</b> member should be set to null.

The values of <b>lpApplicationName</b> and <b>lpAssemblyDirectory</b> are not set to null when the executable creating the activation context is a host for the application. In this case, the host can set a different name for the application to find configuration files, report errors, and so forth.





> [!NOTE]
> The winbase.h header defines ACTCTX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-actctx_section_keyed_data">ACTCTX_SECTION_KEYED_DATA</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createactctxa">CreateActCtx</a>
