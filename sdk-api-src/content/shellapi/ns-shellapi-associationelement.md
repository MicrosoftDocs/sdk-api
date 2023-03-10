---
UID: NS:shellapi.ASSOCIATIONELEMENT
title: ASSOCIATIONELEMENT (shellapi.h)
description: Defines information used by AssocCreateForClasses to retrieve an IQueryAssociations interface for a given file association.
helpviewer_keywords: ["ASSOCCLASS_APP_KEY","ASSOCCLASS_APP_STR","ASSOCCLASS_CLSID_KEY","ASSOCCLASS_CLSID_STR","ASSOCCLASS_FIXED_PROGID_STR","ASSOCCLASS_FOLDER","ASSOCCLASS_PROGID_KEY","ASSOCCLASS_PROGID_STR","ASSOCCLASS_PROTOCOL_STR","ASSOCCLASS_SHELL_KEY","ASSOCCLASS_STAR","ASSOCCLASS_SYSTEM_STR","ASSOCIATIONELEMENT","ASSOCIATIONELEMENT structure [Windows Shell]","_shell_ASSOCIATIONELEMENT","shell.ASSOCIATIONELEMENT","shellapi/ASSOCIATIONELEMENT"]
old-location: shell\ASSOCIATIONELEMENT.htm
tech.root: shell
ms.assetid: 1d1a963f-7ebb-4ba6-9a97-795c8ef11ae4
ms.date: 12/05/2018
ms.keywords: ASSOCCLASS_APP_KEY, ASSOCCLASS_APP_STR, ASSOCCLASS_CLSID_KEY, ASSOCCLASS_CLSID_STR, ASSOCCLASS_FIXED_PROGID_STR, ASSOCCLASS_FOLDER, ASSOCCLASS_PROGID_KEY, ASSOCCLASS_PROGID_STR, ASSOCCLASS_PROTOCOL_STR, ASSOCCLASS_SHELL_KEY, ASSOCCLASS_STAR, ASSOCCLASS_SYSTEM_STR, ASSOCIATIONELEMENT, ASSOCIATIONELEMENT structure [Windows Shell], _shell_ASSOCIATIONELEMENT, shell.ASSOCIATIONELEMENT, shellapi/ASSOCIATIONELEMENT
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: ASSOCIATIONELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ASSOCIATIONELEMENT
 - shellapi/ASSOCIATIONELEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - ASSOCIATIONELEMENT
---

# ASSOCIATIONELEMENT structure


## -description

Defines information used by <a href="/windows/desktop/api/shellapi/nf-shellapi-assoccreateforclasses">AssocCreateForClasses</a> to retrieve an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface for a given file association.

## -struct-fields

### -field ac

Type: <b>ASSOCCLASS</b>

Where to obtain association data and the form the data is stored in. One of the following values from the <b>ASSOCCLASS</b> enumeration.



#### ASSOCCLASS_APP_KEY

The <b>hkClass</b> member provides the full registry path of an application identifier (APPID).



#### ASSOCCLASS_CLSID_KEY

The <b>hkClass</b> member provides the full registry path of a CLSID.



#### ASSOCCLASS_CLSID_STR

The <b>hkClass</b> member names a CLSID found as 
<b>HKEY_CLASSES_ROOT</b>&#92;<b>CLSID</b>&#92;<i>pszClass</i>.
                            



#### ASSOCCLASS_PROGID_KEY

The <b>hkClass</b> member provides the full registry path of a ProgID.



#### ASSOCCLASS_SHELL_KEY

The <b>hkClass</b> member names a key found as                
<b>HKEY_CLASSES_ROOT</b>&#92;<b>SystemFileAssociations</b>&#92;<i>hkClass</i>.
                            



#### ASSOCCLASS_PROGID_STR

The <b>pszClass</b> member names a ProgID found as 
<b>HKEY_CLASSES_ROOT</b>&#92;<i>pszClass</i>.
                            



#### ASSOCCLASS_SYSTEM_STR

The <b>pszClass</b> member names a key found as
<b>HKEY_CLASSES_ROOT</b>&#92;<b>SystemFileAssociations</b>&#92;<i>pszClass</i>.
                            



#### ASSOCCLASS_APP_STR

The APPID storing the application information is found at
<b>HKEY_CLASSES_ROOT</b>&#92;<b>Applications</b>&#92;<i>FileName</i> where <i>FileName</i> is obtained by sending <b>pszClass</b> to <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathfindfilenamea">PathFindFileName</a>.





#### ASSOCCLASS_FOLDER

Use the association information for folders stored under
<b>HKEY_CLASSES_ROOT</b>&#92;<b>Folder</b>. When this flag is set, <b>hkClass</b> and <b>pszClass</b> are ignored.



#### ASSOCCLASS_STAR

Use the association information stored under the 
<b>HKEY_CLASSES_ROOT</b>&#92;<b>*</b> subkey. When this flag is set, <b>hkClass</b> and <b>pszClass</b> are ignored.



#### ASSOCCLASS_FIXED_PROGID_STR

<b>Introduced in Windows 8</b>. Do not use the user defaults to apply the mapping of the class specified by the <b>pszClass</b> member.



#### ASSOCCLASS_PROTOCOL_STR

<b>Introduced in Windows 8</b>. Use the user defaults to apply the mapping of the class specified by the <b>pszClass</b> member; the class is a protocol.

### -field hkClass

Type: <b>HKEY</b>

A registry key that specifies a class that contains association information.

### -field pszClass

Type: <b>PCWSTR</b>

A pointer to the name of a class that contains association information.

## -see-also

<a href="/windows/desktop/shell/fa-progids">Programmatic Identifiers</a>