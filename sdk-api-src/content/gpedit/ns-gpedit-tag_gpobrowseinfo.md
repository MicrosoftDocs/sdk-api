---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tag_GPOBROWSEINFO structure


## -description


The
    <b>GPOBROWSEINFO</b> structure contains information that the 
<a href="https://msdn.microsoft.com/ff144ae4-fc8c-499e-9086-75625b86693c">BrowseForGPO</a> function uses to initialize a GPO browser dialog box. After the user closes the dialog box, the system returns information about the user's actions in this structure.


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




<a href="https://msdn.microsoft.com/ff144ae4-fc8c-499e-9086-75625b86693c">BrowseForGPO</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/8bd42909-7877-414d-a89c-658365acc280">Group Policy Structures</a>
 

 

