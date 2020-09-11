---
UID: NN:shobjidl_core.IApplicationAssociationRegistration
title: IApplicationAssociationRegistration (shobjidl_core.h)
description: Exposes methods that query and set default applications for specific file Association Type, and protocols at a specific Association Level.
helpviewer_keywords: ["IApplicationAssociationRegistration","IApplicationAssociationRegistration interface [Windows Shell]","IApplicationAssociationRegistration interface [Windows Shell]","described","_shell_IApplicationAssociationRegistration","shell.IApplicationAssociationRegistration","shobjidl_core/IApplicationAssociationRegistration"]
old-location: shell\IApplicationAssociationRegistration.htm
tech.root: shell
ms.assetid: 015a3be4-2e74-4a2b-8c02-54dcbf0ecacd
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistration, IApplicationAssociationRegistration interface [Windows Shell], IApplicationAssociationRegistration interface [Windows Shell],described, _shell_IApplicationAssociationRegistration, shell.IApplicationAssociationRegistration, shobjidl_core/IApplicationAssociationRegistration
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationAssociationRegistration
 - shobjidl_core/IApplicationAssociationRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationAssociationRegistration
---

# IApplicationAssociationRegistration interface


## -description

Exposes methods that query and set default applications for specific file <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">Association Type</a>, and protocols at a specific <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel">Association Level</a>.

            
<div class="alert"><b>Note</b>  As of Windows 8, the only functionality of this interface that is supported is <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault">QueryCurrentDefault</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationAssociationRegistration</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApplicationAssociationRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationAssociationRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-clearuserassociations">ClearUserAssociations</a>
</td>
<td align="left" width="63%">
Removes all per-user associations for the current user. This results in a reversion to machine defaults, if they exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault">QueryAppIsDefault</a>
</td>
<td align="left" width="63%">
Determines whether an application owns the registered default association for a given application level and type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall">QueryAppIsDefaultAll</a>
</td>
<td align="left" width="63%">
Determines whether an application owns all of the registered default associations for a given application level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault">QueryCurrentDefault</a>
</td>
<td align="left" width="63%">
Determines the default application for a given association type. This is the default application launched by <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a> for that type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault">SetAppAsDefault</a>
</td>
<td align="left" width="63%">
Sets an application as the default for a given type. For more information, see <a href="https://docs.microsoft.com/windows/desktop/shell/default-programs">Default Programs</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall">SetAppAsDefaultAll</a>
</td>
<td align="left" width="63%">
Sets an application as the default for all of the registered associations of any <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">type</a> for that application.

</td>
</tr>
</table>

## -remarks

Because <b>IApplicationAssociationRegistration</b> is only supported for Windows Vista and Windows 7, applications that support earlier operating systems must use their preexisting code in relation to defaults when running under those operating systems. Those applications should include a check for the operating system version to account for this.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/shell/default-programs">Default Programs</a>

