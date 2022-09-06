---
UID: NE:shlwapi.__unnamed_enum_10
title: FILETYPEATTRIBUTEFLAGS (shlwapi.h)
description: Indicates FILETYPEATTRIBUTEFLAGS constants that are used in the EditFlags value of a file association PROGID registry key.
helpviewer_keywords: ["FILETYPEATTRIBUTEFLAGS","FILETYPEATTRIBUTEFLAGS enumeration [Windows Shell]","FTA_AlwaysUnsafe","FTA_AlwaysUseDirectInvoke","FTA_Exclude","FTA_HasExtension","FTA_NoDDE","FTA_NoEdit","FTA_NoEditDesc","FTA_NoEditDflt","FTA_NoEditIcon","FTA_NoEditMIME","FTA_NoEditVerb","FTA_NoEditVerbCmd","FTA_NoEditVerbExe","FTA_NoNewVerb","FTA_NoRecentDocs","FTA_NoRemove","FTA_NoRemoveVerb","FTA_None","FTA_OpenIsSafe","FTA_SafeForElevation","FTA_Show","shell.FILETYPEATTRIBUTEFLAGS","shell_FILETYPEATTRIBUTEFLAGS","shlwapi/FILETYPEATTRIBUTEFLAGS","shlwapi/FTA_AlwaysUnsafe","shlwapi/FTA_AlwaysUseDirectInvoke","shlwapi/FTA_Exclude","shlwapi/FTA_HasExtension","shlwapi/FTA_NoDDE","shlwapi/FTA_NoEdit","shlwapi/FTA_NoEditDesc","shlwapi/FTA_NoEditDflt","shlwapi/FTA_NoEditIcon","shlwapi/FTA_NoEditMIME","shlwapi/FTA_NoEditVerb","shlwapi/FTA_NoEditVerbCmd","shlwapi/FTA_NoEditVerbExe","shlwapi/FTA_NoNewVerb","shlwapi/FTA_NoRecentDocs","shlwapi/FTA_NoRemove","shlwapi/FTA_NoRemoveVerb","shlwapi/FTA_None","shlwapi/FTA_OpenIsSafe","shlwapi/FTA_SafeForElevation","shlwapi/FTA_Show"]
old-location: shell\FILETYPEATTRIBUTEFLAGS.htm
tech.root: shell
ms.assetid: 63b58659-9c4c-4b39-98d1-743724523dcd
ms.date: 12/05/2018
ms.keywords: FILETYPEATTRIBUTEFLAGS, FILETYPEATTRIBUTEFLAGS enumeration [Windows Shell], FTA_AlwaysUnsafe, FTA_AlwaysUseDirectInvoke, FTA_Exclude, FTA_HasExtension, FTA_NoDDE, FTA_NoEdit, FTA_NoEditDesc, FTA_NoEditDflt, FTA_NoEditIcon, FTA_NoEditMIME, FTA_NoEditVerb, FTA_NoEditVerbCmd, FTA_NoEditVerbExe, FTA_NoNewVerb, FTA_NoRecentDocs, FTA_NoRemove, FTA_NoRemoveVerb, FTA_None, FTA_OpenIsSafe, FTA_SafeForElevation, FTA_Show, shell.FILETYPEATTRIBUTEFLAGS, shell_FILETYPEATTRIBUTEFLAGS, shlwapi/FILETYPEATTRIBUTEFLAGS, shlwapi/FTA_AlwaysUnsafe, shlwapi/FTA_AlwaysUseDirectInvoke, shlwapi/FTA_Exclude, shlwapi/FTA_HasExtension, shlwapi/FTA_NoDDE, shlwapi/FTA_NoEdit, shlwapi/FTA_NoEditDesc, shlwapi/FTA_NoEditDflt, shlwapi/FTA_NoEditIcon, shlwapi/FTA_NoEditMIME, shlwapi/FTA_NoEditVerb, shlwapi/FTA_NoEditVerbCmd, shlwapi/FTA_NoEditVerbExe, shlwapi/FTA_NoNewVerb, shlwapi/FTA_NoRecentDocs, shlwapi/FTA_NoRemove, shlwapi/FTA_NoRemoveVerb, shlwapi/FTA_None, shlwapi/FTA_OpenIsSafe, shlwapi/FTA_SafeForElevation, shlwapi/FTA_Show
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
targetos: Windows
req.typenames: FILETYPEATTRIBUTEFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FILETYPEATTRIBUTEFLAGS
 - shlwapi/FILETYPEATTRIBUTEFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - FILETYPEATTRIBUTEFLAGS
---

# FILETYPEATTRIBUTEFLAGS enumeration


## -description

Indicates <b>FILETYPEATTRIBUTEFLAGS</b> constants that are used in the EditFlags value of a file association <a href="/windows/desktop/shell/fa-progids">PROGID</a> registry key.

## -enum-fields

### -field FTA_None:0x00000000

No <a href="/windows/desktop/api/shlwapi/ne-shlwapi-filetypeattributeflags">FILETYPEATTRIBUTEFLAGS</a> options set.

### -field FTA_Exclude:0x00000001

Excludes the file type.

### -field FTA_Show:0x00000002

Shows file types, such as folders, that are not associated with a file name extension.

### -field FTA_HasExtension:0x00000004

Indicates that the file type has a file name extension.

### -field FTA_NoEdit:0x00000008

Prohibits editing of the registry entries associated with this file type, the addition of new entries, and the deletion or modification of existing entries.

### -field FTA_NoRemove:0x00000010

Prohibits deletion of the registry entries associated with this file type.

### -field FTA_NoNewVerb:0x00000020

Prohibits the addition of new <a href="/windows/desktop/shell/fa-verbs">verbs</a> to the file type.

### -field FTA_NoEditVerb:0x00000040

Prohibits the modification or deletion of canonical <a href="/windows/desktop/shell/fa-verbs">verbs</a> such as <b>open</b> and <b>print</b>.

### -field FTA_NoRemoveVerb:0x00000080

Prohibits the deletion of canonical verbs such as <b>open</b> and <b>print</b>.

### -field FTA_NoEditDesc:0x00000100

Prohibits the modification or deletion of the description of the file type.

### -field FTA_NoEditIcon:0x00000200

Prohibits the modification or deletion of the <a href="/windows/desktop/shell/icon">icon</a> assigned to the file type.

### -field FTA_NoEditDflt:0x00000400

Prohibits the modification of the <a href="/windows/desktop/shell/fa-verbs">default verb</a>.

### -field FTA_NoEditVerbCmd:0x00000800

Prohibits the modification of the <a href="/windows/desktop/shell/fa-verbs">commands</a> associated with verbs.

### -field FTA_NoEditVerbExe:0x00001000

Prohibits the modification or deletion of verbs.

### -field FTA_NoDDE:0x00002000

Prohibits the modification or deletion of the entries related to DDE.

### -field FTA_NoEditMIME:0x00008000

Prohibits the modification or deletion of the content type and default extension entries.

### -field FTA_OpenIsSafe:0x00010000

Indicates that the file type's <b>open</b> verb can be safely invoked for downloaded files. This flag  applies only to safe file types, as identified by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-associsdangerous">AssocIsDangerous</a>. To improve the user experience and reduce unnecessary user prompts when downloading and activating items, file type owners should specify this flag and applications that download and activate files should respect this flag.

### -field FTA_AlwaysUnsafe:0x00020000

Prevents the <b>Never ask me</b> check box from being enabled. Use of this flag means <b>FTA_OpenIsSafe</b> is not respected and <a href="/windows/desktop/api/shlwapi/nf-shlwapi-associsdangerous">AssocIsDangerous</a> always returns TRUE.
If your file type can execute code, you should always use this flag or ensure that the file type handlers mitigate risks, for example, by producing warning prompts before running the code.

The user can override this attribute through the <b>File Type</b> dialog box.

### -field FTA_NoRecentDocs:0x00100000

Prohibits the addition of members of this file type to the <a href="/windows/desktop/shell/manage">Recent Documents</a> folder. Additionally, in Windows 7 and later, prohibits the addition of members of this file type to the automatic <b>Recent</b> or <b>Frequent</b> category of an application's Jump List.

This flag does not restrict members of this file type from being added to a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">custom Jump List</a>. It also places no restriction on the file type being added to the automatic Jump Lists of other applications in the case that other applications use this file type.

### -field FTA_SafeForElevation:0x00200000

<b>Introduced in Windows 8</b>. Marks the file or URI scheme as safe to be used from a low trust application. Files that originate from the Internet or an app container are examples where the file is considered untrusted. Untrusted files that contain code are especially dangerous, and appropriate security mitigations must be applied if the file is to be opened by a full trust application. File type owners for file formats that have the ability to execute code should specify this flag only if their program mitigates elevation-of-privilege threats that are associated with running code at a higher integrity level. Mitigations include prompting the user before code is executed or executing the code with reduced privileges.

By specifying this flag for an entire file type, an app running within an app container can pass files of this type to a program running at full trust. Some file types are recognized as inherently dangerous due to their ability to execute code and will be blocked if you don't specify this value.

### -field FTA_AlwaysUseDirectInvoke:0x00400000

<b>Introduced in Windows 8</b>. Ensures that the verbs for the file type are invoked with a URI instead of a downloaded version of the file. Use this flag only if you've registered the file type's verb to support DirectInvoke through the SupportedProtocols or UseUrl registration.

## -remarks

These flags represent possible attributes stored in the EditFlags value of a ProgID registration. The EditFlags data is a single REG_DWORD.

The following example shows the <b><b>FTA_NoRemove</b></b> (0x00000010) and <b><b>FTA_NoNewVerb</b></b> (0x00000020) attributes assigned to the .myp file type.

<pre><b>HKEY_CLASSES_ROOT</b>
   <b>.myp</b>
      (Default) = MyProgram.1
   <b>MyProgram.1</b>
      (Default) = MyProgram Application
      <b>EditFlags</b> = 0x00000030</pre>\

APIs such as <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata">IQueryAssociations::GetData</a> can retrieve that EditFlags data. Compare the numerical equivalents of these <b>FILETYPEATTRIBUTEFLAGS</b> flags against that retrieved value to determine which flags are set.

The following example demonstrates the use of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata">IQueryAssociations::GetData</a> to determine if those values are set.

                


```
IQueryAssociations *passoc;

HRESULT hr = AssocCreate(CLSID_QueryAssociations, IID_PPV_ARGS(&passoc));
if (SUCCEEDED(hr))
{
    hr = passoc->Init(NULL, pszType, NULL, NULL);
    if (SUCCEEDED(hr))
    {
        DWORD dwEditFlags;
        ULONG cb = sizeof(dwEditFlags);
        
        hr = passoc->GetData(NULL, ASSOCDATA_EDITFLAGS, NULL, &dwEditFlags, &cb);
        if (SUCCEEDED(hr))
        {
            if (dwEditFlags & 0x00000010) // FTA_NoRemove
            {
                // ...
            }    
            if (dwEditFlags & 0x00000020)  // FTA_NoNewVerb
            {
                // ...
            }
        }
    }
    passoc->Release();
}
```


To set an EditFlags attribute, you can use the <a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea">SHSetValue</a> functions. First use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata">IQueryAssociations::GetData</a> to retrieve the current set of attributes as shown in the example above, add the desired <b>FILETYPEATTRIBUTEFLAGS</b> to that value, then write that value back to the registry using one of the two set functions.
