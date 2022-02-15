---
UID: NN:shobjidl.IDesktopGadget
title: IDesktopGadget (shobjidl.h)
description: Exposes a method that allows the programmatic addition of an installed gadget to the user's desktop.
helpviewer_keywords: ["IDesktopGadget","IDesktopGadget interface [Windows Shell]","IDesktopGadget interface [Windows Shell]","described","_shell_IDesktopGadget","shell.IDesktopGadget","shobjidl/IDesktopGadget"]
old-location: shell\IDesktopGadget.htm
tech.root: shell
ms.assetid: 7b3b273a-41ed-4d45-bde9-8250d74d10a9
ms.date: 12/05/2018
ms.keywords: IDesktopGadget, IDesktopGadget interface [Windows Shell], IDesktopGadget interface [Windows Shell],described, _shell_IDesktopGadget, shell.IDesktopGadget, shobjidl/IDesktopGadget
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Sbdrop.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDesktopGadget
 - shobjidl/IDesktopGadget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbdrop.dll
api_name:
 - IDesktopGadget
---

# IDesktopGadget interface


## -description

Exposes a method that allows the programmatic addition of an installed gadget to the user's desktop.

## -inheritance

The <b>IDesktopGadget</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDesktopGadget</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is supplied in Windows as CLSID_DesktopGadget. Third parties do not provide a implementation.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface to run a gadget. A running gadget is displayed on the desktop. This action is often taken at the end of a gadget or application's installation.

## -see-also

[Introduction to the Gadget Platform](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform)
