---
UID: NN:gpedit.IGroupPolicyObject
title: IGroupPolicyObject (gpedit.h)
description: The IGroupPolicyObject interface provides methods to create and modify a GPO directly, without using the Group Policy Object Editor.
helpviewer_keywords: ["IGroupPolicyObject","IGroupPolicyObject interface [Group Policy]","IGroupPolicyObject interface [Group Policy]","described","_win32_igrouppolicyobject","gpedit/IGroupPolicyObject","policy.igrouppolicyobject"]
old-location: policy\igrouppolicyobject.htm
tech.root: Policy
ms.assetid: b3cd31a1-c238-4eb2-8164-9c4891e6227b
ms.date: 12/05/2018
ms.keywords: IGroupPolicyObject, IGroupPolicyObject interface [Group Policy], IGroupPolicyObject interface [Group Policy],described, _win32_igrouppolicyobject, gpedit/IGroupPolicyObject, policy.igrouppolicyobject
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
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGroupPolicyObject
 - gpedit/IGroupPolicyObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject
---

# IGroupPolicyObject interface


## -description

The
    <b>IGroupPolicyObject</b> interface provides methods to create and modify a GPO directly, without using the Group Policy Object Editor.

Note that this interface does not support multithreaded object concurrency.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGroupPolicyObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGroupPolicyObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGroupPolicyObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getdspath">GetDSPath</a>
</td>
<td align="left" width="63%">
Retrieves the Active Directory path to the root of the specified GPO section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getfilesyspath">GetFileSysPath</a>
</td>
<td align="left" width="63%">
Retrieves the file system path (UNC format) to the root of the specified GPO section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getmachinename">GetMachineName</a>
</td>
<td align="left" width="63%">
Retrieves the computer name of the remote GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the unique name for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getoptions">GetOptions</a>
</td>
<td align="left" width="63%">
Retrieves the options for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves the path to the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getpropertysheetpages">GetPropertySheetPages</a>
</td>
<td align="left" width="63%">
Retrieves the property sheet pages associated with the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getregistrykey">GetRegistryKey</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the root of the registry key for the specified GPO section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves type information for the GPO being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-new">New</a>
</td>
<td align="left" width="63%">
Creates a new GPO in the Active Directory with the specified display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-opendsgpo">OpenDSGPO</a>
</td>
<td align="left" width="63%">
Opens the specified GPO and optionally loads the registry information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openlocalmachinegpo">OpenLocalMachineGPO</a>
</td>
<td align="left" width="63%">
Opens the default GPO for the computer and optionally loads the registry information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openremotemachinegpo">OpenRemoteMachineGPO</a>
</td>
<td align="left" width="63%">
Opens the default GPO for the specified remote computer and optionally loads the registry information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-save">Save</a>
</td>
<td align="left" width="63%">
Saves the specified registry policy settings to disk and updates the revision number of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-setdisplayname">SetDisplayName</a>
</td>
<td align="left" width="63%">
Sets the display name for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-setoptions">SetOptions</a>
</td>
<td align="left" width="63%">
Sets the options for the GPO.

</td>
</tr>
</table>

## -remarks

For methods that Microsoft Management Console (MMC) extension snap-ins can use to communicate with the Group Policy Object Editor, see the 
<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>