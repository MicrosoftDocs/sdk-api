---
UID: NE:shlwapi.FILETYPEATTRIBUTEFLAGS
title: FILETYPEATTRIBUTEFLAGS
author: windows-sdk-content
description: Indicates FILETYPEATTRIBUTEFLAGS constants that are used in the EditFlags value of a file association PROGID registry key.
old-location: shell\FILETYPEATTRIBUTEFLAGS.htm
tech.root: shell
ms.assetid: 63b58659-9c4c-4b39-98d1-743724523dcd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FILETYPEATTRIBUTEFLAGS, FILETYPEATTRIBUTEFLAGS enumeration [Windows Shell], FTA_AlwaysUnsafe, FTA_AlwaysUseDirectInvoke, FTA_Exclude, FTA_HasExtension, FTA_NoDDE, FTA_NoEdit, FTA_NoEditDesc, FTA_NoEditDflt, FTA_NoEditIcon, FTA_NoEditMIME, FTA_NoEditVerb, FTA_NoEditVerbCmd, FTA_NoEditVerbExe, FTA_NoNewVerb, FTA_NoRecentDocs, FTA_NoRemove, FTA_NoRemoveVerb, FTA_None, FTA_OpenIsSafe, FTA_SafeForElevation, FTA_Show, shell.FILETYPEATTRIBUTEFLAGS, shell_FILETYPEATTRIBUTEFLAGS, shlwapi/FILETYPEATTRIBUTEFLAGS, shlwapi/FTA_AlwaysUnsafe, shlwapi/FTA_AlwaysUseDirectInvoke, shlwapi/FTA_Exclude, shlwapi/FTA_HasExtension, shlwapi/FTA_NoDDE, shlwapi/FTA_NoEdit, shlwapi/FTA_NoEditDesc, shlwapi/FTA_NoEditDflt, shlwapi/FTA_NoEditIcon, shlwapi/FTA_NoEditMIME, shlwapi/FTA_NoEditVerb, shlwapi/FTA_NoEditVerbCmd, shlwapi/FTA_NoEditVerbExe, shlwapi/FTA_NoNewVerb, shlwapi/FTA_NoRecentDocs, shlwapi/FTA_NoRemove, shlwapi/FTA_NoRemoveVerb, shlwapi/FTA_None, shlwapi/FTA_OpenIsSafe, shlwapi/FTA_SafeForElevation, shlwapi/FTA_Show
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - FILETYPEATTRIBUTEFLAGS
product: Windows
targetos: Windows
req.typenames: FILETYPEATTRIBUTEFLAGS
req.redist: 
---

# FILETYPEATTRIBUTEFLAGS enumeration


## -description


Indicates <b>FILETYPEATTRIBUTEFLAGS</b> constants that are used in the EditFlags value of a file association <a href="https://msdn.microsoft.com/f2b666d6-bf22-47b5-87e1-8de5ff51c152">PROGID</a> registry key.


## -enum-fields




### -field FTA_None

No <a href="https://msdn.microsoft.com/63b58659-9c4c-4b39-98d1-743724523dcd">FILETYPEATTRIBUTEFLAGS</a> options set.


### -field FTA_Exclude

Excludes the file type.


### -field FTA_Show

Shows file types, such as folders, that are not associated with a file name extension.


### -field FTA_HasExtension

Indicates that the file type has a file name extension.


### -field FTA_NoEdit

Prohibits editing of the registry entries associated with this file type, the addition of new entries, and the deletion or modification of existing entries.


### -field FTA_NoRemove

Prohibits deletion of the registry entries associated with this file type.


### -field FTA_NoNewVerb

Prohibits the addition of new <a href="https://msdn.microsoft.com/4f46b8c3-1e12-447c-87f4-bbe2c305f77a">verbs</a> to the file type.


### -field FTA_NoEditVerb

Prohibits the modification or deletion of canonical <a href="https://msdn.microsoft.com/4f46b8c3-1e12-447c-87f4-bbe2c305f77a">verbs</a> such as <b>open</b> and <b>print</b>.


### -field FTA_NoRemoveVerb

Prohibits the deletion of canonical verbs such as <b>open</b> and <b>print</b>.


### -field FTA_NoEditDesc

Prohibits the modification or deletion of the description of the file type.


### -field FTA_NoEditIcon

Prohibits the modification or deletion of the <a href="https://msdn.microsoft.com/1827239c-0588-45aa-b7be-f96fb7affa65">icon</a> assigned to the file type.


### -field FTA_NoEditDflt

Prohibits the modification of the <a href="https://msdn.microsoft.com/4f46b8c3-1e12-447c-87f4-bbe2c305f77a">default verb</a>.


### -field FTA_NoEditVerbCmd

Prohibits the modification of the <a href="https://msdn.microsoft.com/4f46b8c3-1e12-447c-87f4-bbe2c305f77a">commands</a> associated with verbs.


### -field FTA_NoEditVerbExe

Prohibits the modification or deletion of verbs.


### -field FTA_NoDDE

Prohibits the modification or deletion of the entries related to DDE.


### -field FTA_NoEditMIME

Prohibits the modification or deletion of the content type and default extension entries.


### -field FTA_OpenIsSafe

Indicates that the file type's <b>open</b> verb can be safely invoked for downloaded files. This flag  applies only to safe file types, as identified by <a href="https://msdn.microsoft.com/4e0bc3ce-f9d2-4766-8b19-c0954d71e890">AssocIsDangerous</a>. To improve the user experience and reduce unnecessary user prompts when downloading and activating items, file type owners should specify this flag and applications that download and activate files should respect this flag.


### -field FTA_AlwaysUnsafe

Prevents the <b>Never ask me</b> check box from being enabled. Use of this flag means <b>FTA_OpenIsSafe</b> is not respected and <a href="https://msdn.microsoft.com/4e0bc3ce-f9d2-4766-8b19-c0954d71e890">AssocIsDangerous</a> always returns TRUE.
If your file type can execute code, you should always use this flag or ensure that the file type handlers mitigate risks, for example, by producing warning prompts before running the code.

The user can override this attribute through the <b>File Type</b> dialog box.


### -field FTA_NoRecentDocs

Prohibits the addition of members of this file type to the <a href="https://msdn.microsoft.com/d9ffda6f-adc0-44a3-b410-e23bf5f4f165">Recent Documents</a> folder. Additionally, in Windows 7 and later, prohibits the addition of members of this file type to the automatic <b>Recent</b> or <b>Frequent</b> category of an application's Jump List.

This flag does not restrict members of this file type from being added to a <a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">custom Jump List</a>. It also places no restriction on the file type being added to the automatic Jump Lists of other applications in the case that other applications use this file type.


### -field FTA_SafeForElevation

<b>Introduced in Windows 8</b>. Marks the file as safe to be passed from a low trust application to a full trust application. Files that originate from the Internet or an app container are examples where the file is considered untrusted. Untrusted files that contain code are especially dangerous, and appropriate security mitigations must be applied if the file is to be opened by a full trust application. File type owners for file formats that have the ability to execute code should specify this flag only if their program mitigates elevation-of-privilege threats that are associated with running code at a higher integrity level. Mitigations include prompting the user before code is executed or executing the code with reduced privileges.

By specifying this flag for an entire file type, an app running within an app container can pass files of this type to a program running at full trust. Some file types are recognized as inherently dangerous due to their ability to execute code and will be blocked if you don't specify this value.


### -field FTA_AlwaysUseDirectInvoke

<b>Introduced in Windows 8</b>. Ensures that the verbs for the file type are invoked with a URI instead of a downloaded version of the file. Use this flag only if you've registered the file type's verb to support DirectInvoke through the SupportedProtocols or UseUrl registration.


## -remarks



These flags represent possible attributes stored in the EditFlags value of a ProgID registration. The EditFlags data is a single REG_DWORD.

The following example shows the <b><b>FTA_NoRemove</b></b> (0x00000010) and <b><b>FTA_NoNewVerb</b></b> (0x00000020) attributes assigned to the .myp file type.
	
            	<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>.myp</b>
      (Default) = MyProgram.1
   <b>MyProgram.1</b>
      (Default) = MyProgram Application
      <b>EditFlags</b> = 0x00000030</pre>


APIs such as <a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">IQueryAssociations::GetData</a> can retrieve that EditFlags data. Compare the numerical equivalents of these <b>FILETYPEATTRIBUTEFLAGS</b> flags against that retrived value to determine which flags are set.

The following example demonstrates the use of <a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">IQueryAssociations::GetData</a> to determine if those values are set.

                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IQueryAssociations *passoc;

HRESULT hr = AssocCreate(CLSID_QueryAssociations, IID_PPV_ARGS(&amp;passoc));
if (SUCCEEDED(hr))
{
    hr = passoc-&gt;Init(NULL, pszType, NULL, NULL);
    if (SUCCEEDED(hr))
    {
        DWORD dwEditFlags;
        ULONG cb = sizeof(dwEditFlags);
        
        hr = passoc-&gt;GetData(NULL, ASSOCDATA_EDITFLAGS, NULL, &amp;dwEditFlags, &amp;cb);
        if (SUCCEEDED(hr))
        {
            if (dwEditFlags &amp; 0x00000010) // FTA_NoRemove
            {
                // ...
            }    
            if (dwEditFlags &amp; 0x00000020)  // FTA_NoNewVerb
            {
                // ...
            }
        }
    }
    passoc-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>
To set an EditFlags attribute, you can use the <a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a> or <a href="https://msdn.microsoft.com/6cd5b7fd-8fb9-4c24-9670-20c23ca709bf">SHSetValue</a> functions. First use <a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">IQueryAssociations::GetData</a> to retrieve the current set of attributes as shown in the example above, add the desired <b>FILETYPEATTRIBUTEFLAGS</b> to that value, then write that value back to the registry using one of the two set functions.



