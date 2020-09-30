---
UID: NS:gpedit.tag_GPOBROWSEINFO
title: GPOBROWSEINFO (gpedit.h)
description: The GPOBROWSEINFO structure contains information that the BrowseForGPO function uses to initialize a GPO browser dialog box. After the user closes the dialog box, the system returns information about the user's actions in this structure.
helpviewer_keywords: ["*LPGPOBROWSEINFO","GPHintDomain","GPHintMachine","GPHintOrganizationalUnit","GPHintSite","GPHintUnknown","GPOBROWSEINFO","GPOBROWSEINFO structure [Group Policy]","GPOTypeDS","GPOTypeLocal","GPOTypeRemote","GPO_BROWSE_DISABLE_NEW","GPO_BROWSE_INITTOALL","GPO_BROWSE_NOCOMPUTERS","GPO_BROWSE_NODSGPOS","GPO_BROWSE_OPENBUTTON","LPGPOBROWSEINFO","LPGPOBROWSEINFO structure pointer [Group Policy]","_win32_gpobrowseinfo_str","gpedit/GPOBROWSEINFO","gpedit/LPGPOBROWSEINFO","policy.gpobrowseinfo_str"]
old-location: policy\gpobrowseinfo_str.htm
tech.root: Policy
ms.assetid: a0d038f2-66f1-4a79-b9e7-189cb57b80a9
ms.date: 12/05/2018
ms.keywords: '*LPGPOBROWSEINFO, GPHintDomain, GPHintMachine, GPHintOrganizationalUnit, GPHintSite, GPHintUnknown, GPOBROWSEINFO, GPOBROWSEINFO structure [Group Policy], GPOTypeDS, GPOTypeLocal, GPOTypeRemote, GPO_BROWSE_DISABLE_NEW, GPO_BROWSE_INITTOALL, GPO_BROWSE_NOCOMPUTERS, GPO_BROWSE_NODSGPOS, GPO_BROWSE_OPENBUTTON, LPGPOBROWSEINFO, LPGPOBROWSEINFO structure pointer [Group Policy], _win32_gpobrowseinfo_str, gpedit/GPOBROWSEINFO, gpedit/LPGPOBROWSEINFO, policy.gpobrowseinfo_str'
req.header: gpedit.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GPOBROWSEINFO, *LPGPOBROWSEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_GPOBROWSEINFO
 - gpedit/tag_GPOBROWSEINFO
 - LPGPOBROWSEINFO
 - gpedit/LPGPOBROWSEINFO
 - GPOBROWSEINFO
 - gpedit/GPOBROWSEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gpedit.h
api_name:
 - GPOBROWSEINFO
---

# GPOBROWSEINFO structure


## -description

The
    <b>GPOBROWSEINFO</b> structure contains information that the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-browseforgpo">BrowseForGPO</a> function uses to initialize a GPO browser dialog box. After the user closes the dialog box, the system returns information about the user's actions in this structure.

## -struct-fields

### -field dwSize

Specifies the size of the structure, in bytes.

### -field dwFlags

Specifies dialog box options. This member can be one or more of the following values.



#### GPO_BROWSE_DISABLE_NEW

Disables the ability to create a new GPO on any tab other than the <b>All</b> tab.



#### GPO_BROWSE_NOCOMPUTERS

Removes the <b>Computers</b> tab.



#### GPO_BROWSE_NODSGPOS

Removes the <b>Domain/OU</b> and <b>Sites</b> tabs.



#### GPO_BROWSE_OPENBUTTON

Changes the <b>OK</b> button to <b>Open</b>.



#### GPO_BROWSE_INITTOALL

Initializes the dialog box with focus on the <b>All</b> tab.

### -field hwndOwner

Specifies the handle to the parent window. If this member is <b>NULL</b>, the dialog box has no owner.

### -field lpTitle

Specifies the title bar text. If this member is <b>NULL</b>, the title bar text is <b>Browse for a Group Policy Object</b>.

### -field lpInitialOU

Specifies the initial domain or organizational unit.

### -field lpDSPath

Pointer to a buffer that receives the Active Directory path of the GPO.

### -field dwDSPathSize

Specifies the size, in characters, of the <b>lpDSPath</b> buffer.

### -field lpName

Pointer to a buffer that receives either the computer name or the friendly (display) name of the GPO. If the user opens or creates a GPO in the <b>Computers</b> tab, this member contains the computer name. If the user opens or creates a GPO in the Active Directory, this member contains the friendly name. To determine the GPO type, see the description for the <b>gpoType</b> member.

This member can be <b>NULL</b>.

### -field dwNameSize

Specifies the size, in characters, of the <b>lpName</b> buffer.

### -field gpoType

Receives the GPO type. This member can be one of the following values.



#### GPOTypeLocal

Local



#### GPOTypeRemote

Remote



#### GPOTypeDS

Active Directory

### -field gpoHint

Receives a hint about the Active Directory container to which the GPO might be linked. This member can be one of the following values.



#### GPHintUnknown

No link information is available.



#### GPHintMachine

The object might be linked to a computer (local or remote).



#### GPHintSite

The object might be linked to a site.



#### GPHintDomain

The object might be linked to a domain.



#### GPHintOrganizationalUnit

The object might be linked to an organizational unit.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-browseforgpo">BrowseForGPO</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>