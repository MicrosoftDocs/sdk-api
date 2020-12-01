---
UID: NN:gpedit.IGPEInformation
title: IGPEInformation (gpedit.h)
description: The IGPEInformation interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the Group Policy Object Editor. For more information about MMC, see the Microsoft Management Console.
helpviewer_keywords: ["IGPEInformation","IGPEInformation interface [Group Policy]","IGPEInformation interface [Group Policy]","described","_win32_igpeinformation","gpedit/IGPEInformation","policy.igpeinformation"]
old-location: policy\igpeinformation.htm
tech.root: Policy
ms.assetid: 3b3e7793-fc69-43a3-a2b1-0aa36748a19b
ms.date: 12/05/2018
ms.keywords: IGPEInformation, IGPEInformation interface [Group Policy], IGPEInformation interface [Group Policy],described, _win32_igpeinformation, gpedit/IGPEInformation, policy.igpeinformation
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
 - IGPEInformation
 - gpedit/IGPEInformation
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
 - IGPEInformation
---

# IGPEInformation interface


## -description

The
    <b>IGPEInformation</b> interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the Group Policy Object Editor. For more information about MMC, see the 
<a href="/previous-versions/windows/desktop/mmc/mmc-programmer-s-guide">Microsoft Management Console</a>.

Note that this interface does not support multithreaded object concurrency.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPEInformation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGPEInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPEInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getdisplayname">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for a GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getdspath">GetDSPath</a>
</td>
<td align="left" width="63%">
Retrieves the Active Directory path for a section of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getfilesyspath">GetFileSysPath</a>
</td>
<td align="left" width="63%">
Returns the file system path for a section of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-gethint">GetHint</a>
</td>
<td align="left" width="63%">
Retrieves the type of Active Directory object to which a GPO can be linked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the unique name for a GPO, usually a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getoptions">GetOptions</a>
</td>
<td align="left" width="63%">
Retrieves the options the user has selected for the Group Policy Object Editor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getregistrykey">GetRegistryKey</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the root of the registry key for a section of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves type information for the GPO being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-policychanged">PolicyChanged</a>
</td>
<td align="left" width="63%">
Informs the Group Policy Object Editor that policy settings have changed.

</td>
</tr>
</table>

## -remarks

To create and modify a GPO directly, without using the Group Policy Object Editor, see the methods of the 
<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>