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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationAssociationRegistrationUI
 - shobjidl/IApplicationAssociationRegistrationUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IApplicationAssociationRegistrationUI
---

# IApplicationAssociationRegistrationUI interface


## -description

Exposes a method that launches an advanced association dialog box through which the user can customize their associations.

## -inheritance

The <b>IApplicationAssociationRegistrationUI</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApplicationAssociationRegistrationUI</b> also has these types of members:

## -remarks

Because <b>IApplicationAssociationRegistrationUI</b> is only supported for Windows Vista and later, applications that support earlier operating systems must use their preexisting code when running under those operating systems. Those applications should include a check for the operating system version to account for this.

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>
