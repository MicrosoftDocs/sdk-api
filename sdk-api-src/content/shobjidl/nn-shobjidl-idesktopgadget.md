---
UID: NN:shobjidl.IDesktopGadget
title: IDesktopGadget (shobjidl.h)
author: windows-sdk-content
description: Exposes a method that allows the programmatic addition of an installed gadget to the user's desktop.
old-location: shell\IDesktopGadget.htm
tech.root: shell
ms.assetid: 7b3b273a-41ed-4d45-bde9-8250d74d10a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDesktopGadget, IDesktopGadget interface [Windows Shell], IDesktopGadget interface [Windows Shell],described, _shell_IDesktopGadget, shell.IDesktopGadget, shobjidl/IDesktopGadget
ms.topic: interface
f1_keywords: 
 - "shobjidl/IDesktopGadget"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbdrop.dll
api_name:
 - IDesktopGadget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDesktopGadget interface


## -description


Exposes a method that allows the programmatic addition of an installed gadget to the user's desktop.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDesktopGadget</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDesktopGadget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDesktopGadget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-idesktopgadget-rungadget">RunGadget</a>
</td>
<td align="left" width="63%">
Adds an installed gadget to the desktop.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is supplied in Windows as CLSID_DesktopGadget. Third parties do not provide a implementation.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface to run a gadget. A running gadget is displayed on the desktop. This action is often taken at the end of a gadget or application's installation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform">Introduction to the Gadget Platform</a>
 

 

