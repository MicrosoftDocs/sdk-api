---
UID: NF:winreg.RegSaveKeyExA
title: RegSaveKeyExA function
author: windows-sdk-content
description: Saves the specified key and all of its subkeys and values to a registry file, in the specified format.
old-location: base\regsavekeyex.htm
old-project: SysInfo
ms.assetid: f93b4162-cac4-42f7-bfd4-9e23fff80a03
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: REG_LATEST_FORMAT, REG_NO_COMPRESSION, REG_STANDARD_FORMAT, RegSaveKeyEx, RegSaveKeyEx function, RegSaveKeyExA, RegSaveKeyExW, _win32_regsavekeyex, base.regsavekeyex, winreg/RegSaveKeyEx, winreg/RegSaveKeyExA, winreg/RegSaveKeyExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegSaveKeyExW (Unicode) and RegSaveKeyExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-Core-Localregistry-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Registry-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
-	MinKernelBase.dll
-	api-ms-win-core-registry-l1-1-1.dll
api_name:
-	RegSaveKeyEx
-	RegSaveKeyExA
-	RegSaveKeyExW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegSaveKeyExA function


## -description


Saves the specified key and all of its subkeys and values to a registry file, in the specified format.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to an open registry key. 

This function does not support the <b>HKEY_CLASSES_ROOT</b> predefined key.


### -param lpFile [in]

The name of the file in which the specified key and subkeys are to be saved. If the file already exists, the function fails. 




The new file has the archive attribute.

If the string does not include a path, the file is created in the current directory of the calling process for a local key, or in the %systemroot%\system32 directory for a remote key.


### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new file. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the file gets a default security descriptor. The ACLs in a default security descriptor for a file are inherited from its parent directory.


### -param Flags [in]

The format of the saved key or hive. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_STANDARD_FORMAT"></a><a id="reg_standard_format"></a><dl>
<dt><b>REG_STANDARD_FORMAT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The key or hive is saved in standard format. The standard format is the only format supported by Windows 2000.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_LATEST_FORMAT"></a><a id="reg_latest_format"></a><dl>
<dt><b>REG_LATEST_FORMAT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The key or hive is saved in the latest format. The latest format is supported starting with Windows XP. After the key or hive is saved in this format, it cannot be loaded on an earlier system.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NO_COMPRESSION"></a><a id="reg_no_compression"></a><dl>
<dt><b>REG_NO_COMPRESSION</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The hive is saved with no compression, for faster save operations. The <i>hKey</i> parameter must specify the root of a hive under <b>HKEY_LOCAL_MACHINE </b> or <b>HKEY_USERS</b>. For example, <b>HKLM\SOFTWARE</b> is the root of a hive.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

If more than one of the possible values listed above for the <i>Flags</i> parameter is specified in one call to this function—for example, if two or more values are OR'ed— or if REG_NO_COMPRESSION is specified and <i>hKey</i> specifies a key that is not the root of a hive, this function returns ERROR_INVALID_PARAMETER.




## -remarks



Unlike <a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>, this function does not support the <b>HKEY_CLASSES_ROOT</b> predefined key.

If <i>hKey</i> represents a key on a remote computer, the path described by <i>lpFile</i> is relative to the remote computer.

The 
<b>RegSaveKeyEx</b> function saves only nonvolatile keys. It does not save volatile keys. A key is made volatile or nonvolatile at its creation; see 
<b>RegCreateKeyEx</b>.

You can use the file created by 
<b>RegSaveKeyEx</b> in subsequent calls to the 
<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a>, 
<a href="https://msdn.microsoft.com/f968fa71-edc8-4f49-b9fa-1e89224df33b">RegReplaceKey</a>, or 
<a href="https://msdn.microsoft.com/6267383d-427a-4ae8-b9cc-9c1861d3b7bb">RegRestoreKey</a> function. If 
<b>RegSaveKeyEx</b> fails partway through its operation, the file will be corrupt and subsequent calls to 
<b>RegLoadKey</b>, 
<b>RegReplaceKey</b>, or 
<b>RegRestoreKey</b> for the file will fail.


				Using <b>RegSaveKeyEx</b> together with 
<a href="https://msdn.microsoft.com/6267383d-427a-4ae8-b9cc-9c1861d3b7bb">RegRestoreKey</a> to copy subtrees in the registry is not recommended. This method does not trigger notifications and can invalidate handles used by other applications. Instead, use the 
<a href="https://msdn.microsoft.com/52521ef4-fe59-4766-8828-acb557b0e968">SHCopyKey</a> function or the <a href="https://msdn.microsoft.com/d16f2b47-e537-42b0-90b3-9f9a00e61e76">RegCopyTree</a> function.

The calling process must have the SE_BACKUP_NAME privilege enabled. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a>



<a href="https://msdn.microsoft.com/f968fa71-edc8-4f49-b9fa-1e89224df33b">RegReplaceKey</a>



<a href="https://msdn.microsoft.com/6267383d-427a-4ae8-b9cc-9c1861d3b7bb">RegRestoreKey</a>



<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>



<a href="https://msdn.microsoft.com/a71a564d-934a-46e8-b555-989a6fa82337">Registry Files</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

