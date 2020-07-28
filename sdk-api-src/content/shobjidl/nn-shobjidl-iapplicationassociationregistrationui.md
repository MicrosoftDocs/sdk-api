---
UID: NN:shobjidl.IApplicationAssociationRegistrationUI
title: IApplicationAssociationRegistrationUI (shobjidl.h)
description: Exposes a method that launches an advanced association dialog box through which the user can customize their associations.
helpviewer_keywords: ["IApplicationAssociationRegistrationUI","IApplicationAssociationRegistrationUI interface [Windows Shell]","IApplicationAssociationRegistrationUI interface [Windows Shell]","described","_shell_IApplicationAssociationRegistrationUI","shell.IApplicationAssociationRegistrationUI","shobjidl/IApplicationAssociationRegistrationUI"]
old-location: shell\IApplicationAssociationRegistrationUI.htm
tech.root: shell
ms.assetid: 3a4d6f1d-72c2-4bd0-ad44-1c42a5bf9cb6
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistrationUI, IApplicationAssociationRegistrationUI interface [Windows Shell], IApplicationAssociationRegistrationUI interface [Windows Shell],described, _shell_IApplicationAssociationRegistrationUI, shell.IApplicationAssociationRegistrationUI, shobjidl/IApplicationAssociationRegistrationUI
f1_keywords:
- shobjidl/IApplicationAssociationRegistrationUI
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- IApplicationAssociationRegistrationUI
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IApplicationAssociationRegistrationUI interface


## -description


Exposes a method that launches an advanced association dialog box through which the user can customize their associations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationAssociationRegistrationUI</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApplicationAssociationRegistrationUI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationAssociationRegistrationUI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui">LaunchAdvancedAssociationUI</a>
</td>
<td align="left" width="63%">
Launches an advanced association dialog box through which the user can customize the associations for the application specified in <i>pszAppRegName</i>.

</td>
</tr>
</table> 


## -remarks



Because <b>IApplicationAssociationRegistrationUI</b> is only supported for Windows Vista and later, applications that support earlier operating systems must use their preexisting code when running under those operating systems. Those applications should include a check for the operating system version to account for this.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/default-programs">Default Programs</a>
 

 

